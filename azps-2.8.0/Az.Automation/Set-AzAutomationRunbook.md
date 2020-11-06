---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 4dd1eee278adcced1dbace9a30e88b5767037746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613675"
---
# <span data-ttu-id="1bcf6-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="1bcf6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bcf6-102">SYNOPSIS</span></span>
<span data-ttu-id="1bcf6-103">修改 runbook。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-103">Modifies a runbook.</span></span>

## <span data-ttu-id="1bcf6-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bcf6-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bcf6-105">說明</span><span class="sxs-lookup"><span data-stu-id="1bcf6-105">DESCRIPTION</span></span>
<span data-ttu-id="1bcf6-106">AzAutomationRunbook Cmdlet 會修改 AP 中 Azure 自動化 runbook 的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="1bcf6-107">示例</span><span class="sxs-lookup"><span data-stu-id="1bcf6-107">EXAMPLES</span></span>

### <span data-ttu-id="1bcf6-108">範例1：針對 runbook 啟用詳細記錄</span><span class="sxs-lookup"><span data-stu-id="1bcf6-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1bcf6-109">這個命令會針對在名為 Contoso17 的 Azure 自動化帳戶中指定的 runbook 啟用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1bcf6-110">參數</span><span class="sxs-lookup"><span data-stu-id="1bcf6-110">PARAMETERS</span></span>

### <span data-ttu-id="1bcf6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1bcf6-111">-AutomationAccountName</span></span>
<span data-ttu-id="1bcf6-112">指定此 Cmdlet 修改 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="1bcf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bcf6-113">-DefaultProfile</span></span>
<span data-ttu-id="1bcf6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1bcf6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bcf6-115">-描述</span><span class="sxs-lookup"><span data-stu-id="1bcf6-115">-Description</span></span>
<span data-ttu-id="1bcf6-116">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="1bcf6-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="1bcf6-117">-LogProgress</span></span>
<span data-ttu-id="1bcf6-118">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="1bcf6-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="1bcf6-119">-LogVerbose</span></span>
<span data-ttu-id="1bcf6-120">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="1bcf6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1bcf6-121">-Name</span></span>
<span data-ttu-id="1bcf6-122">指定此 Cmdlet 修改的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1bcf6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bcf6-123">-ResourceGroupName</span></span>
<span data-ttu-id="1bcf6-124">指定此 Cmdlet 修改 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="1bcf6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bcf6-125">-Tag</span></span>
<span data-ttu-id="1bcf6-126">[Runbook] 標記。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-126">The runbook tags.</span></span>

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

### <span data-ttu-id="1bcf6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bcf6-127">CommonParameters</span></span>
<span data-ttu-id="1bcf6-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bcf6-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bcf6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1bcf6-130">INPUTS</span></span>

### <span data-ttu-id="1bcf6-131">System.object</span><span class="sxs-lookup"><span data-stu-id="1bcf6-131">System.String</span></span>

### <span data-ttu-id="1bcf6-132">System.object</span><span class="sxs-lookup"><span data-stu-id="1bcf6-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="1bcf6-133">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1bcf6-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1bcf6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1bcf6-134">OUTPUTS</span></span>

### <span data-ttu-id="1bcf6-135">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="1bcf6-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="1bcf6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1bcf6-136">NOTES</span></span>

## <span data-ttu-id="1bcf6-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bcf6-137">RELATED LINKS</span></span>

[<span data-ttu-id="1bcf6-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="1bcf6-139">AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="1bcf6-140">匯入-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="1bcf6-141">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1bcf6-142">新-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1bcf6-143">發佈-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="1bcf6-144">移除-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="1bcf6-145">開始-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bcf6-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


