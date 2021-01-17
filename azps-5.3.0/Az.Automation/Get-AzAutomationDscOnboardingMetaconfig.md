---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447351"
---
# <span data-ttu-id="ea8bd-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="ea8bd-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="ea8bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8bd-103">建立元設定. mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="ea8bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea8bd-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea8bd-105">DESCRIPTION</span></span>
<span data-ttu-id="ea8bd-106">**AzAutomationDscOnboardingMetaconfig** Cmdlet 會建立 Ap 所需的狀態設定 (DSC) 元設定管理物件格式 (MOF) 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="ea8bd-107">這個 Cmdlet 會針對您指定的每個電腦名稱稱建立一個 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="ea8bd-108">這個 Cmdlet 會為 mof 檔案建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="ea8bd-109">您可以執行此資料夾的 Set-DscLocalConfigurationManager Cmdlet，以將這些電腦作為 DSC 節點的 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="ea8bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="ea8bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ea8bd-111">範例1：自動化 DSC 的板載伺服器</span><span class="sxs-lookup"><span data-stu-id="ea8bd-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="ea8bd-112">第一個命令會針對自動帳戶（名為 Contoso17）的兩個伺服器建立 DSC 元配置檔案。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="ea8bd-113">該命令會將這些檔案儲存在桌面上。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="ea8bd-114">第二個命令使用 **DscLocalConfigurationManager** Cmdlet，將元設定套用至指定的電腦，以將其作為 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="ea8bd-115">參數</span><span class="sxs-lookup"><span data-stu-id="ea8bd-115">PARAMETERS</span></span>

### <span data-ttu-id="ea8bd-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ea8bd-116">-AutomationAccountName</span></span>
<span data-ttu-id="ea8bd-117">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="ea8bd-118">您可以將 *ComputerName* 參數指定的電腦上建到此參數指定的帳號。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ea8bd-119">-ComputerName</span></span>
<span data-ttu-id="ea8bd-120">指定此 Cmdlet 產生的電腦名稱稱的陣列。 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="ea8bd-121">如果您沒有指定此參數，則 Cmdlet 會為目前電腦 (localhost) 產生一個 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8bd-122">-DefaultProfile</span></span>
<span data-ttu-id="ea8bd-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ea8bd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ea8bd-124">-Force</span></span>
<span data-ttu-id="ea8bd-125">強制執行命令，不會提示您確認，以及取代現有的、具有相同名稱的 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ea8bd-126">-OutputFolder</span></span>
<span data-ttu-id="ea8bd-127">指定此 Cmdlet 儲存. mof 檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8bd-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea8bd-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ea8bd-130">這個 Cmdlet 會在此參數指定的資源群組中，將 mof 檔案建立給板載電腦。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ea8bd-131">-Confirm</span></span>
<span data-ttu-id="ea8bd-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8bd-133">-WhatIf</span></span>
<span data-ttu-id="ea8bd-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8bd-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8bd-136">CommonParameters</span></span>
<span data-ttu-id="ea8bd-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8bd-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea8bd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8bd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ea8bd-139">INPUTS</span></span>

### <span data-ttu-id="ea8bd-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ea8bd-140">System.String</span></span>

### <span data-ttu-id="ea8bd-141">System.object []</span><span class="sxs-lookup"><span data-stu-id="ea8bd-141">System.String[]</span></span>

## <span data-ttu-id="ea8bd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ea8bd-142">OUTPUTS</span></span>

### <span data-ttu-id="ea8bd-143">DscOnboardingMetaconfig 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ea8bd-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="ea8bd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ea8bd-144">NOTES</span></span>

## <span data-ttu-id="ea8bd-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea8bd-145">RELATED LINKS</span></span>
