---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: e520fec3d0299ca2b5f74bb2a8a8b7de437d7a2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916445"
---
# <span data-ttu-id="52769-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="52769-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="52769-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52769-102">SYNOPSIS</span></span>
<span data-ttu-id="52769-103">建立元組式 .mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="52769-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="52769-104">語法</span><span class="sxs-lookup"><span data-stu-id="52769-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52769-105">描述</span><span class="sxs-lookup"><span data-stu-id="52769-105">DESCRIPTION</span></span>
<span data-ttu-id="52769-106">**Get-AzAutomationDscOnboardingMetaconfig** Cmdlet 會建立 APS 想要的狀態組態 (DSC) 元組態 Managed 物件格式 (MOF) 檔案。</span><span class="sxs-lookup"><span data-stu-id="52769-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="52769-107">此 Cmdlet 會針對您指定的每個電腦名稱稱建立 .mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="52769-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="52769-108">Cmdlet 會建立 .mof 檔案的資料夾。</span><span class="sxs-lookup"><span data-stu-id="52769-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="52769-109">您可以針對此資料夾Set-DscLocalConfigurationManager Cmdlet，以將這些電腦以 DSC 節點的 Azure 自動化帳戶登錄。</span><span class="sxs-lookup"><span data-stu-id="52769-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="52769-110">例子</span><span class="sxs-lookup"><span data-stu-id="52769-110">EXAMPLES</span></span>

### <span data-ttu-id="52769-111">範例 1：將伺服器設置至 Automation DSC</span><span class="sxs-lookup"><span data-stu-id="52769-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="52769-112">第一個命令會為名為 Contoso17 的自動化帳戶建立兩個伺服器的 DSC 元組設定檔。</span><span class="sxs-lookup"><span data-stu-id="52769-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="52769-113">該命令會將這些檔案保存在桌面上。</span><span class="sxs-lookup"><span data-stu-id="52769-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="52769-114">第二個命令使用 **Set-DscLocalConfigurationManager** Cmdlet，將元設定套用至指定的電腦，將它們設為 DSC 節點。</span><span class="sxs-lookup"><span data-stu-id="52769-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="52769-115">參數</span><span class="sxs-lookup"><span data-stu-id="52769-115">PARAMETERS</span></span>

### <span data-ttu-id="52769-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="52769-116">-AutomationAccountName</span></span>
<span data-ttu-id="52769-117">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="52769-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="52769-118">您可以將 *ComputerName* 參數指定給此參數指定之帳戶的電腦上板。</span><span class="sxs-lookup"><span data-stu-id="52769-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="52769-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="52769-119">-ComputerName</span></span>
<span data-ttu-id="52769-120">指定此 Cmdlet 會產生 .mof 檔案的電腦名稱稱陣列。</span><span class="sxs-lookup"><span data-stu-id="52769-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="52769-121">如果您未指定此參數，Cmdlet 會針對目前使用本地主機 (.mof) 。</span><span class="sxs-lookup"><span data-stu-id="52769-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="52769-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52769-122">-DefaultProfile</span></span>
<span data-ttu-id="52769-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="52769-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52769-124">-強制</span><span class="sxs-lookup"><span data-stu-id="52769-124">-Force</span></span>
<span data-ttu-id="52769-125">強制執行命令而不提示您確認，並取代名稱相同的現有 .mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="52769-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="52769-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="52769-126">-OutputFolder</span></span>
<span data-ttu-id="52769-127">指定此 Cmdlet 儲存 .mof 檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="52769-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="52769-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52769-128">-ResourceGroupName</span></span>
<span data-ttu-id="52769-129">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52769-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="52769-130">此 Cmdlet 會建立 .mof 檔案，以將電腦設置在此參數指定的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="52769-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52769-131">-確認</span><span class="sxs-lookup"><span data-stu-id="52769-131">-Confirm</span></span>
<span data-ttu-id="52769-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="52769-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52769-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52769-133">-WhatIf</span></span>
<span data-ttu-id="52769-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52769-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52769-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52769-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52769-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52769-136">CommonParameters</span></span>
<span data-ttu-id="52769-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52769-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52769-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="52769-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52769-139">輸入</span><span class="sxs-lookup"><span data-stu-id="52769-139">INPUTS</span></span>

### <span data-ttu-id="52769-140">System.String</span><span class="sxs-lookup"><span data-stu-id="52769-140">System.String</span></span>

### <span data-ttu-id="52769-141">System.String[]</span><span class="sxs-lookup"><span data-stu-id="52769-141">System.String[]</span></span>

## <span data-ttu-id="52769-142">輸出</span><span class="sxs-lookup"><span data-stu-id="52769-142">OUTPUTS</span></span>

### <span data-ttu-id="52769-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="52769-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="52769-144">筆記</span><span class="sxs-lookup"><span data-stu-id="52769-144">NOTES</span></span>

## <span data-ttu-id="52769-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="52769-145">RELATED LINKS</span></span>
