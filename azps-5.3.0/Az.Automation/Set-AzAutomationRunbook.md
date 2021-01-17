---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447108"
---
# <span data-ttu-id="bfcfe-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="bfcfe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bfcfe-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcfe-103">修改 runbook。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-103">Modifies a runbook.</span></span>

## <span data-ttu-id="bfcfe-104">句法</span><span class="sxs-lookup"><span data-stu-id="bfcfe-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfcfe-105">說明</span><span class="sxs-lookup"><span data-stu-id="bfcfe-105">DESCRIPTION</span></span>
<span data-ttu-id="bfcfe-106">AzAutomationRunbook Cmdlet 會修改 AP 中 Azure 自動化 runbook 的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="bfcfe-107">示例</span><span class="sxs-lookup"><span data-stu-id="bfcfe-107">EXAMPLES</span></span>

### <span data-ttu-id="bfcfe-108">範例1：針對 runbook 啟用詳細記錄</span><span class="sxs-lookup"><span data-stu-id="bfcfe-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bfcfe-109">這個命令會針對在名為 Contoso17 的 Azure 自動化帳戶中指定的 runbook 啟用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="bfcfe-110">參數</span><span class="sxs-lookup"><span data-stu-id="bfcfe-110">PARAMETERS</span></span>

### <span data-ttu-id="bfcfe-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bfcfe-111">-AutomationAccountName</span></span>
<span data-ttu-id="bfcfe-112">指定此 Cmdlet 修改 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="bfcfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcfe-113">-DefaultProfile</span></span>
<span data-ttu-id="bfcfe-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bfcfe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfcfe-115">-描述</span><span class="sxs-lookup"><span data-stu-id="bfcfe-115">-Description</span></span>
<span data-ttu-id="bfcfe-116">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="bfcfe-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="bfcfe-117">-LogProgress</span></span>
<span data-ttu-id="bfcfe-118">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcfe-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="bfcfe-119">-LogVerbose</span></span>
<span data-ttu-id="bfcfe-120">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcfe-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="bfcfe-121">-Name</span></span>
<span data-ttu-id="bfcfe-122">指定此 Cmdlet 修改的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcfe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcfe-123">-ResourceGroupName</span></span>
<span data-ttu-id="bfcfe-124">指定此 Cmdlet 修改 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="bfcfe-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bfcfe-125">-Tag</span></span>
<span data-ttu-id="bfcfe-126">[Runbook] 標記。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcfe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcfe-127">CommonParameters</span></span>
<span data-ttu-id="bfcfe-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcfe-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcfe-130">輸入</span><span class="sxs-lookup"><span data-stu-id="bfcfe-130">INPUTS</span></span>

### <span data-ttu-id="bfcfe-131">System.object</span><span class="sxs-lookup"><span data-stu-id="bfcfe-131">System.String</span></span>

### <span data-ttu-id="bfcfe-132">System.object</span><span class="sxs-lookup"><span data-stu-id="bfcfe-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="bfcfe-133">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bfcfe-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bfcfe-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bfcfe-134">OUTPUTS</span></span>

### <span data-ttu-id="bfcfe-135">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="bfcfe-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="bfcfe-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bfcfe-136">NOTES</span></span>

## <span data-ttu-id="bfcfe-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="bfcfe-137">RELATED LINKS</span></span>

[<span data-ttu-id="bfcfe-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="bfcfe-139">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="bfcfe-140">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="bfcfe-141">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="bfcfe-142">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="bfcfe-143">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="bfcfe-144">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="bfcfe-145">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcfe-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


