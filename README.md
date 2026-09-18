<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Título da Página e Meta Tags para Pré-visualização no WhatsApp -->
    <title>Ficha de Cadastramento - CF Waldir Vieira</title>
    <meta name="description" content="Formulário Digital de Cadastramento Familiar - Clínica da Família Waldir Vieira (SMS/RJ)">
    <meta property="og:title" content="Ficha de Cadastramento - CF Waldir Vieira">
    <meta property="og:description" content="Acesse e preencha a ficha de cadastramento familiar e domiciliar.">
    <meta property="og:type" content="website">

    <style>
        :root {
            --forms-purple: #673ab7;
            --forms-bg: #f0ebf8;
            --card-bg: #ffffff;
            --text-main: #202124;
            --text-secondary: #5f6368;
            --border-light: #dadce0;
            --required-red: #d93025;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Roboto', Arial, sans-serif;
        }

        body {
            background-color: var(--forms-bg);
            color: var(--text-main);
            padding: 20px 10px;
            display: flex;
            justify-content: center;
        }

        .forms-container {
            width: 100%;
            max-width: 820px;
        }

        .forms-header-card {
            background-color: var(--card-bg);
            border-radius: 8px;
            border-top: 10px solid var(--forms-purple);
            padding: 24px;
            margin-bottom: 12px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.12);
        }

        .forms-header-card h1 {
            font-size: 1.8rem;
            color: var(--text-main);
            margin-bottom: 8px;
        }

        .forms-header-card p {
            font-size: 0.9rem;
            color: var(--text-secondary);
            line-height: 1.4;
        }

        .req-notice {
            color: var(--required-red);
            font-size: 0.85rem;
            margin-top: 10px;
        }

        .forms-card {
            background-color: var(--card-bg);
            border-radius: 8px;
            padding: 24px;
            margin-bottom: 12px;
            border: 1px solid var(--border-light);
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }

        .forms-card-title {
            font-size: 1.1rem;
            font-weight: 500;
            color: var(--forms-purple);
            margin-bottom: 16px;
            padding-bottom: 8px;
            border-bottom: 2px solid #f0ebf8;
        }

        .grid-row {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 16px;
            margin-bottom: 16px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-size: 0.88rem;
            color: var(--text-main);
            margin-bottom: 6px;
            font-weight: 500;
        }

        .required-asterisk {
            color: var(--required-red);
            margin-left: 2px;
        }

        .form-group input, 
        .form-group select, 
        .form-group textarea {
            padding: 10px 12px;
            border: 1px solid var(--border-light);
            border-radius: 4px;
            font-size: 0.95rem;
            outline: none;
            background-color: #fafafa;
            transition: border-color 0.2s, background-color 0.2s;
        }

        .form-group input:focus, 
        .form-group select:focus, 
        .form-group textarea:focus {
            border-color: var(--forms-purple);
            background-color: #fff;
        }

        .form-group input[readonly] {
            background-color: #e9ecef;
            color: #495057;
            cursor: not-allowed;
            font-weight: 500;
        }

        .checkbox-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 10px;
            margin-top: 8px;
            background-color: #fcfaff;
            padding: 15px;
            border-radius: 6px;
            border: 1px solid #e0d6f3;
        }

        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
            cursor: pointer;
        }

        .checkbox-item input[type="checkbox"] {
            width: 16px;
            height: 16px;
            accent-color: var(--forms-purple);
            cursor: pointer;
        }

        .specify-input {
            margin-top: 8px;
            display: none;
        }

        .btn-action {
            background-color: var(--forms-purple);
            color: white;
            border: none;
            padding: 10px 24px;
            font-size: 0.95rem;
            font-weight: 500;
            border-radius: 4px;
            cursor: pointer;
            transition: opacity 0.2s;
        }

        .btn-action:hover {
            opacity: 0.9;
        }

        .btn-submit {
            background-color: #2e7d32;
            width: 100%;
            padding: 14px;
            font-size: 1rem;
            font-weight: bold;
            margin-top: 10px;
        }

        .section-header {
            background-color: #ede7f6;
            color: var(--forms-purple);
            padding: 12px 16px;
            border-radius: 6px;
            font-weight: bold;
            margin-bottom: 16px;
            font-size: 1rem;
        }
    </style>
</head>
<body>

<div class="forms-container">
    <div class="forms-header-card">
        <h1>Ficha de Cadastramento - Clínica da Família Waldir Vieira</h1>
        <p>Secretaria Municipal de Saúde do Rio de Janeiro - SMS/RJ</p>
        <p class="req-notice">* Indica campo obrigatório</p>
    </div>

    <form id="fichaAForm" onsubmit="salvarFicha(event)">

        <!-- UNIDADE E SELEÇÃO DE EQUIPE DA CLÍNICA -->
        <div class="forms-card">
            <div class="forms-card-title">Dados da Unidade de Saúde</div>
            <div class="grid-row">
                <div class="form-group">
                    <label>Unidade de Saúde:</label>
                    <input type="text" value="Clínica da Família Waldir Vieira" readonly>
                </div>
                <div class="form-group">
                    <label>Área Programática (AP):</label>
                    <input type="text" value="4.0" readonly>
                </div>
                <div class="form-group">
                    <label>Sua Equipe de Saúde <span class="required-asterisk">*</span>:</label>
                    <select id="areaEquipe" required>
                        <option value="">Selecione a sua Equipe...</option>
                        <option value="1 - Equipe Boiuna">1 - Equipe Boiuna</option>
                        <option value="2 - Equipe Biólogos">2 - Equipe Biólogos</option>
                        <option value="3 - Equipe Garden">3 - Equipe Garden</option>
                        <option value="4 - Equipe Waldir Vieira">4 - Equipe Waldir Vieira</option>
                        <option value="5 - Equipe São Sebastião">5 - Equipe São Sebastião</option>
                        <option value="6 - Equipe Ariperana">6 - Equipe Ariperana</option>
                        <option value="7 - Equipe Rosa do Povo">7 - Equipe Rosa do Povo</option>
                        <option value="8 - Equipe Lagolândia">8 - Equipe Lagolândia</option>
                        <option value="9 - Equipe Noel Nutels">9 - Equipe Noel Nutels</option>
                    </select>
                </div>
            </div>
        </div>

        <!-- CONDICIONAL INICIAL: QUANTITATIVO DE MORADORES -->
        <div class="forms-card">
            <div class="forms-card-title">1. Quantitativo de Residentes</div>
            <div class="form-group">
                <label for="qtdMoradores">Quantos moradores residem neste domicílio? <span class="required-asterisk">*</span></label>
                <div style="display: flex; gap: 10px; margin-top: 8px;">
                    <input type="number" id="qtdMoradores" min="1" max="20" placeholder="Ex: 3" style="max-width: 200px;" required>
                    <button type="button" class="btn-action" onclick="desdobrarFormulario()">Abrir Formulários</button>
                </div>
            </div>
        </div>

        <!-- SEÇÃO DOMICÍLIO -->
        <div id="secaoDomicilio" class="forms-card" style="display: none;">
            <div class="forms-card-title">2. Endereço e Dados do Domicílio</div>
            
            <div class="grid-row">
                <div class="form-group">
                    <label>Endereço / Logradouro <span class="required-asterisk">*</span>:</label>
                    <input type="text" id="dom_endereco" placeholder="Rua, Av, Travessa..." required>
                </div>
                <div class="form-group">
                    <label>Número <span class="required-asterisk">*</span>:</label>
                    <input type="text" id="dom_numero" placeholder="Nº da casa" required>
                </div>
                <div class="form-group">
                    <label>Complemento <span class="required-asterisk">*</span>:</label>
                    <input type="text" id="dom_complemento" placeholder="Apto, Bloco, Casa 2..." required>
                </div>
            </div>

            <div class="grid-row">
                <div class="form-group">
                    <label>CEP <span class="required-asterisk">*</span>:</label>
                    <input type="text" id="dom_cep" placeholder="00000-000" required>
                </div>
                <div class="form-group">
                    <label>Número de Telefone / Contato <span class="required-asterisk">*</span>:</label>
                    <input type="tel" id="dom_contato" placeholder="(21) 90000-0000" required>
                </div>
            </div>

            <div class="forms-card-title" style="margin-top: 15px; font-size: 1rem;">Condições Sanitárias e Domiciliares (Opcionais)</div>

            <div class="grid-row">
                <div class="form-group">
                    <label>Tipo de Domicílio:</label>
                    <select id="dom_tipo" onchange="toggleOutrosSelect(this, 'dom_tipo_outro')">
                        <option value="">Selecione...</option>
                        <option value="1">Tijolo / Alvenaria</option>
                        <option value="2">Taipa Revestida</option>
                        <option value="3">Taipa Não Revestida</option>
                        <option value="4">Madeira</option>
                        <option value="5">Material Aproveitado</option>
                        <option value="outro">Outro (Especificar)</option>
                    </select>
                    <input type="text" id="dom_tipo_outro" class="specify-input" placeholder="Especifique o tipo de domicílio">
                </div>
                <div class="form-group">
                    <label>Nº de Cômodos:</label>
                    <input type="number" id="dom_comodos" min="1">
                </div>
                <div class="form-group">
                    <label>Energia Elétrica:</label>
                    <select id="dom_energia">
                        <option value="">Selecione...</option>
                        <option value="1">Sim</option>
                        <option value="0">Não</option>
                    </select>
                </div>
            </div>

            <div class="grid-row">
                <div class="form-group">
                    <label>Abastecimento de Água:</label>
                    <select id="dom_agua" onchange="toggleOutrosSelect(this, 'dom_agua_outro')">
                        <option value="">Selecione...</option>
                        <option value="1">Rede Pública</option>
                        <option value="2">Poço ou Nascente</option>
                        <option value="outro">Outro (Especificar)</option>
                    </select>
                    <input type="text" id="dom_agua_outro" class="specify-input" placeholder="Especifique a fonte de água">
                </div>
                <div class="form-group">
                    <label>Tratamento da Água:</label>
                    <select id="dom_trat_agua">
                        <option value="">Selecione...</option>
                        <option value="1">Filtração</option>
                        <option value="2">Cloração</option>
                        <option value="3">Fervura</option>
                        <option value="4">Sem Tratamento</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>Destino do Esgoto Sanitário:</label>
                    <select id="dom_esgoto">
                        <option value="">Selecione...</option>
                        <option value="1">Rede Pública</option>
                        <option value="2">Fossa</option>
                        <option value="3">Céu Aberto</option>
                    </select>
                </div>
            </div>

            <div class="grid-row">
                <div class="form-group">
                    <label>Destino do Lixo:</label>
                    <select id="dom_lixo">
                        <option value="">Selecione...</option>
                        <option value="1">Coletado</option>
                        <option value="2">Queimado / Enterrado</option>
                        <option value="3">Céu Aberto</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>Renda Familiar (Salários Mínimos):</label>
                    <select id="dom_renda">
                        <option value="">Selecione...</option>
                        <option value="1">Até 1/4 SM</option>
                        <option value="2">Mais de 1/4 até 1/2 SM</option>
                        <option value="3">Mais de 1/2 até 1 SM</option>
                        <option value="4">Mais de 1 até 2 SM</option>
                        <option value="5">Mais de 2 até 5 SM</option>
                        <option value="6">Mais de 5 SM</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>Melhor Horário / Dia para Atendimento:</label>
                    <input type="text" id="dom_visitas" placeholder="Ex: Manhã / Sábado">
                </div>
            </div>
        </div>

        <!-- CONTAINER DOS MORADORES -->
        <div id="containerMoradores"></div>

        <!-- BOTÃO FINAL DE SUBMISSÃO -->
        <div id="secaoSalvar" class="forms-card" style="display: none;">
            <button type="submit" id="btnSubmitForm" class="btn-action btn-submit">Concluir e Salvar Cadastro de Moradores</button>
        </div>

    </form>
</div>

<script>
    const URL_APPS_SCRIPT = "https://script.google.com/macros/s/AKfycbwSH_KxRiCjDu8BJBknURiTBdfhxAVOnUcwNvv8hlf7BHhbOo2fUwHSUQauggb--xJ0/exec";

    function toggleOutrosSelect(selectElement, targetId) {
        const targetInput = document.getElementById(targetId);
        if (selectElement.value === 'outro') {
            targetInput.style.display = 'block';
        } else {
            targetInput.style.display = 'none';
            targetInput.value = '';
        }
    }

    function toggleCheckboxSpecify(checkbox, targetId) {
        const targetInput = document.getElementById(targetId);
        if (checkbox.checked) {
            targetInput.style.display = 'block';
        } else {
            targetInput.style.display = 'none';
            targetInput.value = '';
        }
    }

    function desdobrarFormulario() {
        const qtdInput = document.getElementById('qtdMoradores');
        const qtd = parseInt(qtdInput.value);
        const container = document.getElementById('containerMoradores');
        const secaoDomicilio = document.getElementById('secaoDomicilio');
        const secaoSalvar = document.getElementById('secaoSalvar');

        if (isNaN(qtd) || qtd < 1 || qtd > 20) {
            alert('Por favor, informe uma quantidade válida de moradores (entre 1 e 20).');
            return;
        }

        secaoDomicilio.style.display = 'block';
        secaoSalvar.style.display = 'block';

        let htmlBuffer = '';

        for (let i = 1; i <= qtd; i++) {
            htmlBuffer += `
            <div class="forms-card">
                <div class="section-header">Morador nº ${i} ${i === 1 ? '(Responsável Familiar / Usuário Principal)' : '(Dependente / Usuário)'}</div>
                
                <div class="grid-row">
                    <div class="form-group">
                        <label>Nome da Pessoa <span class="required-asterisk">*</span>:</label>
                        <input type="text" id="nome_${i}" required placeholder="Nome completo do morador">
                    </div>
                    <div class="form-group">
                        <label>Data de Nascimento <span class="required-asterisk">*</span>:</label>
                        <input type="date" id="dataNasc_${i}" required>
                    </div>
                    <div class="form-group">
                        <label>Sexo <span class="required-asterisk">*</span>:</label>
                        <select id="sexo_${i}" required>
                            <option value="">Selecione...</option>
                            <option value="M">Masculino</option>
                            <option value="F">Feminino</option>
                        </select>
                    </div>
                </div>

                <div class="grid-row">
                    <div class="form-group">
                        <label>Raça / Cor <span class="required-asterisk">*</span>:</label>
                        <select id="raca_${i}" required>
                            <option value="">Selecione...</option>
                            <option value="branca">Branca</option>
                            <option value="preta">Preta</option>
                            <option value="parda">Parda</option>
                            <option value="amarela">Amarela</option>
                            <option value="indigena">Indígena</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Nome da Mãe <span class="required-asterisk">*</span>:</label>
                        <input type="text" id="mae_${i}" required placeholder="Nome completo da mãe">
                    </div>
                    <div class="form-group">
                        <label>Nome do Pai (Opcional):</label>
                        <input type="text" id="pai_${i}" placeholder="Nome completo do pai">
                    </div>
                </div>

                <div class="forms-card-title" style="margin-top: 10px; font-size: 1rem;">Informações Sociais e Religiosas</div>
                <div class="grid-row">
                    <div class="form-group">
                        <label>Religião / Crença:</label>
                        <select id="religiao_${i}" onchange="toggleOutrosSelect(this, 'religiao_outra_${i}')">
                            <option value="">Selecione...</option>
                            <option value="sem_religiao">Sem religião</option>
                            <option value="catolico">Católico</option>
                            <option value="evangelico">Evangélico</option>
                            <option value="espirita">Espírita</option>
                            <option value="umbanda">Umbanda / Candomblé</option>
                            <option value="islamismo">Islamismo</option>
                            <option value="budista">Budista</option>
                            <option value="judaismo">Judaísmo</option>
                            <option value="outro">Outra (Especificar)</option>
                        </select>
                        <input type="text" id="religiao_outra_${i}" class="specify-input" placeholder="Especifique a religião/crença">
                    </div>

                    <div class="form-group">
                        <label>Beneficiário do BPC (Benefício de Prestação Continuada)?</label>
                        <select id="bpc_${i}">
                            <option value="">Selecione...</option>
                            <option value="nao">Não</option>
                            <option value="sim">Sim</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <label>Possui Plano de Saúde Privado / Convênio?</label>
                        <select id="plano_saude_${i}">
                            <option value="">Selecione...</option>
                            <option value="nao">Não</option>
                            <option value="sim">Sim</option>
                        </select>
                    </div>
                </div>

                <div class="forms-card-title" style="margin-top: 15px; font-size: 1rem;">Doenças ou Condições de Saúde Referidas</div>
                <p style="font-size: 0.85rem; color: #5f6368; margin-bottom: 8px;">Marque todas as condições presentes ou relatadas pelo morador:</p>
                
                <div class="checkbox-grid">
                    <label class="checkbox-item"><input type="checkbox" id="cond_alcohol_${i}"> Alcoolismo</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_aids_${i}"> AIDS / HIV</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_asma_${i}"> Asma</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_cancer_${i}"> Câncer</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_chagas_${i}"> Doença de Chagas</label>
                    
                    <label class="checkbox-item"><input type="checkbox" id="cond_def_fisica_${i}"> Deficiência Física</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_def_mental_${i}"> Deficiência Mental / Intelectual</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_def_visual_${i}"> Deficiência Visual</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_def_auditiva_${i}"> Deficiência Auditiva</label>
                    
                    <label class="checkbox-item"><input type="checkbox" id="cond_diabetes_${i}"> Diabetes Mellitus</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_transtorno_mental_${i}"> Transtorno Mental</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_epilepsia_${i}"> Epilepsia</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_gestante_${i}"> Gestante</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_hipertensao_${i}"> Hipertensão Arterial (HAS)</label>
                    
                    <label class="checkbox-item"><input type="checkbox" id="cond_hanseniase_${i}"> Hanseníase</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_malaria_${i}"> Malária</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_tuberculose_${i}"> Tuberculose</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_violencia_${i}"> Violência Doméstica</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_suicidio_${i}"> Tentativa de Suicídio</label>
                    
                    <label class="checkbox-item"><input type="checkbox" id="cond_drogas_${i}"> Usuário de Drogas Ilícitas</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_psicofarmacos_${i}"> Usuário de Psicofármacos</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_internacao_psi_${i}"> Internação Psiquiátrica (últimos 12 meses)</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_resp_${i}"> Sintomático Respiratório</label>
                    <label class="checkbox-item"><input type="checkbox" id="cond_dermato_${i}"> Sintomático Dermatológico</label>
                    
                    <label class="checkbox-item">
                        <input type="checkbox" id="cond_outros_check_${i}" onchange="toggleCheckboxSpecify(this, 'cond_outros_text_${i}')"> Outros
                    </label>
                </div>
                <input type="text" id="cond_outros_text_${i}" class="specify-input" placeholder="Especifique a outra condição ou doença">

                <div class="forms-card-title" style="margin-top: 20px; font-size: 1rem;">Documentos e Outras Informações (Opcionais)</div>

                <div class="grid-row">
                    <div class="form-group">
                        <label>CPF:</label>
                        <input type="text" id="cpf_${i}" placeholder="000.000.000-00">
                    </div>
                    <div class="form-group">
                        <label>Cartão Nacional de Saúde (CNS / SUS):</label>
                        <input type="text" id="cns_${i}" placeholder="000 0000 0000 0000">
                    </div>
                    <div class="form-group">
                        <label>NIS (se houver):</label>
                        <input type="text" id="nis_${i}" placeholder="Número de Identificação Social">
                    </div>
                </div>

                <div class="grid-row">
                    <div class="form-group">
                        <label>Beneficiário Bolsa Família?</label>
                        <select id="bolsaFam_${i}">
                            <option value="">Selecione...</option>
                            <option value="nao">Não</option>
                            <option value="sim">Sim</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Beneficiário Cartão Família Carioca?</label>
                        <select id="cartaoCarioca_${i}">
                            <option value="">Selecione...</option>
                            <option value="nao">Não</option>
                            <option value="sim">Sim</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Frequenta Escola?</label>
                        <select id="escola_${i}">
                            <option value="">Selecione...</option>
                            <option value="sim">Sim</option>
                            <option value="nao">Não</option>
                        </select>
                    </div>
                </div>

                <div class="grid-row">
                    <div class="form-group">
                        <label>Ocupação / Profissão:</label>
                        <input type="text" id="ocupacao_${i}" placeholder="Ex: Pedreiro, Estudante, Aposentado">
                    </div>
                    <div class="form-group">
                        <label>Escolaridade:</label>
                        <select id="escolaridade_${i}">
                            <option value="">Selecione...</option>
                            <option value="1">Sem Instrução</option>
                            <option value="2">Fundamental Incompleto</option>
                            <option value="3">Fundamental Completo</option>
                            <option value="4">Médio Incompleto</option>
                            <option value="5">Médio Completo</option>
                            <option value="6">Superior Completo</option>
                        </select>
                    </div>
                </div>
            </div>`;
        }

        container.innerHTML = htmlBuffer;
        secaoDomicilio.scrollIntoView({ behavior: 'smooth' });
    }

    function salvarFicha(event) {
        event.preventDefault();

        const btnSubmit = document.getElementById('btnSubmitForm');
        const qtd = parseInt(document.getElementById('qtdMoradores').value);
        const equipeSel = document.getElementById('areaEquipe').value;

        if (!equipeSel) {
            alert('Por favor, selecione qual é a sua Equipe antes de enviar.');
            return;
        }

        if (!qtd) {
            alert('Por favor, informe a quantidade de moradores.');
            return;
        }

        btnSubmit.disabled = true;
        btnSubmit.innerText = 'Enviando cadastro...';

        const fichaCompleta = {
            unidadeSaude: "Clínica da Família Waldir Vieira",
            ap: "4.0",
            area: equipeSel,
            domicilio: {
                endereco: document.getElementById('dom_endereco').value,
                numero: document.getElementById('dom_numero').value,
                complemento: document.getElementById('dom_complemento').value,
                cep: document.getElementById('dom_cep').value,
                contato: document.getElementById('dom_contato').value,
                tipo: document.getElementById('dom_tipo').value === 'outro' ? document.getElementById('dom_tipo_outro').value : document.getElementById('dom_tipo').value,
                comodos: document.getElementById('dom_comodos').value,
                energia: document.getElementById('dom_energia').value,
                agua: document.getElementById('dom_agua').value === 'outro' ? document.getElementById('dom_agua_outro').value : document.getElementById('dom_agua').value,
                tratAgua: document.getElementById('dom_trat_agua').value,
                esgoto: document.getElementById('dom_esgoto').value,
                lixo: document.getElementById('dom_lixo').value,
                renda: document.getElementById('dom_renda').value,
                visita: document.getElementById('dom_visitas').value
            },
            moradores: []
        };

        for (let i = 1; i <= qtd; i++) {
            fichaCompleta.moradores.push({
                ordem: i,
                nome: document.getElementById(`nome_${i}`).value,
                dataNascimento: document.getElementById(`dataNasc_${i}`).value,
                sexo: document.getElementById(`sexo_${i}`).value,
                raca: document.getElementById(`raca_${i}`).value,
                mae: document.getElementById(`mae_${i}`).value,
                pai: document.getElementById(`pai_${i}`).value,
                religiao: document.getElementById(`religiao_${i}`).value === 'outro' ? document.getElementById(`religiao_outra_${i}`).value : document.getElementById(`religiao_${i}`).value,
                bpc: document.getElementById(`bpc_${i}`).value,
                planoSaude: document.getElementById(`plano_saude_${i}`).value,
                condicoesSaude: {
                    alcoolismo: document.getElementById(`cond_alcohol_${i}`).checked,
                    aids: document.getElementById(`cond_aids_${i}`).checked,
                    asma: document.getElementById(`cond_asma_${i}`).checked,
                    cancer: document.getElementById(`cond_cancer_${i}`).checked,
                    chagas: document.getElementById(`cond_chagas_${i}`).checked,
                    deficienciaFisica: document.getElementById(`cond_def_fisica_${i}`).checked,
                    deficienciaMental: document.getElementById(`cond_def_mental_${i}`).checked,
                    deficienciaVisual: document.getElementById(`cond_def_visual_${i}`).checked,
                    deficienciaAuditiva: document.getElementById(`cond_def_auditiva_${i}`).checked,
                    diabetes: document.getElementById(`cond_diabetes_${i}`).checked,
                    transtornoMental: document.getElementById(`cond_transtorno_mental_${i}`).checked,
                    epilepsia: document.getElementById(`cond_epilepsia_${i}`).checked,
                    gestante: document.getElementById(`cond_gestante_${i}`).checked,
                    hipertensao: document.getElementById(`cond_hipertensao_${i}`).checked,
                    hanseniase: document.getElementById(`cond_hanseniase_${i}`).checked,
                    malaria: document.getElementById(`cond_malaria_${i}`).checked,
                    tuberculose: document.getElementById(`cond_tuberculose_${i}`).checked,
                    violenciaDomestica: document.getElementById(`cond_violencia_${i}`).checked,
                    tentativaSuicidio: document.getElementById(`cond_suicidio_${i}`).checked,
                    drogasIlicitas: document.getElementById(`cond_drogas_${i}`).checked,
                    psicofarmacos: document.getElementById(`cond_psicofarmacos_${i}`).checked,
                    internacaoPsiquiatrica: document.getElementById(`cond_internacao_psi_${i}`).checked,
                    sintomaticoRespiratorio: document.getElementById(`cond_resp_${i}`).checked,
                    sintomaticoDermatologico: document.getElementById(`cond_dermato_${i}`).checked,
                    outros: document.getElementById(`cond_outros_check_${i}`).checked ? document.getElementById(`cond_outros_text_${i}`).value : null
                },
                cpf: document.getElementById(`cpf_${i}`).value,
                cns: document.getElementById(`cns_${i}`).value,
                nis: document.getElementById(`nis_${i}`).value,
                bolsaFamilia: document.getElementById(`bolsaFam_${i}`).value,
                cartaoCarioca: document.getElementById(`cartaoCarioca_${i}`).value,
                frequentaEscola: document.getElementById(`escola_${i}`).value,
                ocupacao: document.getElementById(`ocupacao_${i}`).value,
                escolaridade: document.getElementById(`escolaridade_${i}`).value
            });
        }

        fetch(URL_APPS_SCRIPT, {
            method: "POST",
            mode: "no-cors",
            headers: {
                "Content-Type": "application/json"
            },
            body: JSON.stringify(fichaCompleta)
        })
        .then(() => {
            alert(`Cadastro enviado com sucesso para a equipe "${equipeSel}"!`);
            btnSubmit.disabled = false;
            btnSubmit.innerText = 'Concluir e Salvar Cadastro de Moradores';
            document.getElementById('fichaAForm').reset();
            document.getElementById('containerMoradores').innerHTML = '';
            document.getElementById('secaoDomicilio').style.display = 'none';
            document.getElementById('secaoSalvar').style.display = 'none';
        })
        .catch(err => {
            alert("Erro ao enviar dados para a planilha: " + err);
            btnSubmit.disabled = false;
            btnSubmit.innerText = 'Concluir e Salvar Cadastro de Moradores';
        });
    }
</script>

</body>
</html>