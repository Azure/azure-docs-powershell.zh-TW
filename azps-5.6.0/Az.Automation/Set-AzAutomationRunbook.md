---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 26a84b381e3193f9f95f21135f40489f0cacb754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915634"
---
# <span data-ttu-id="09156-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="09156-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09156-102">SYNOPSIS</span></span>
<span data-ttu-id="09156-103">修改執行簿。</span><span class="sxs-lookup"><span data-stu-id="09156-103">Modifies a runbook.</span></span>

## <span data-ttu-id="09156-104">語法</span><span class="sxs-lookup"><span data-stu-id="09156-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09156-105">描述</span><span class="sxs-lookup"><span data-stu-id="09156-105">DESCRIPTION</span></span>
<span data-ttu-id="09156-106">**Set-AzAutomationRunbook** Cmdlet 會修改 APS 中 Azure Automation Runbook 的設定。</span><span class="sxs-lookup"><span data-stu-id="09156-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="09156-107">例子</span><span class="sxs-lookup"><span data-stu-id="09156-107">EXAMPLES</span></span>

### <span data-ttu-id="09156-108">範例 1：為 runbook 啟用詳細記錄</span><span class="sxs-lookup"><span data-stu-id="09156-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="09156-109">此命令會針對 Azure Automation 帳戶 Contoso17 中指定 runbook 的工作啟用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="09156-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="09156-110">參數</span><span class="sxs-lookup"><span data-stu-id="09156-110">PARAMETERS</span></span>

### <span data-ttu-id="09156-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="09156-111">-AutomationAccountName</span></span>
<span data-ttu-id="09156-112">指定此 Cmdlet 修改 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="09156-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="09156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09156-113">-DefaultProfile</span></span>
<span data-ttu-id="09156-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="09156-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09156-115">-描述</span><span class="sxs-lookup"><span data-stu-id="09156-115">-Description</span></span>
<span data-ttu-id="09156-116">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="09156-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="09156-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="09156-117">-LogProgress</span></span>
<span data-ttu-id="09156-118">指定 runbook 記錄是否進行。</span><span class="sxs-lookup"><span data-stu-id="09156-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="09156-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="09156-119">-LogVerbose</span></span>
<span data-ttu-id="09156-120">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="09156-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="09156-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="09156-121">-Name</span></span>
<span data-ttu-id="09156-122">指定此 Cmdlet 修改之 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="09156-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="09156-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09156-123">-ResourceGroupName</span></span>
<span data-ttu-id="09156-124">指定此 Cmdlet 修改 Runbook 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="09156-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="09156-125">-標記</span><span class="sxs-lookup"><span data-stu-id="09156-125">-Tag</span></span>
<span data-ttu-id="09156-126">Runbook 標記。</span><span class="sxs-lookup"><span data-stu-id="09156-126">The runbook tags.</span></span>

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

### <span data-ttu-id="09156-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09156-127">CommonParameters</span></span>
<span data-ttu-id="09156-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09156-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09156-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="09156-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09156-130">輸入</span><span class="sxs-lookup"><span data-stu-id="09156-130">INPUTS</span></span>

### <span data-ttu-id="09156-131">System.String</span><span class="sxs-lookup"><span data-stu-id="09156-131">System.String</span></span>

### <span data-ttu-id="09156-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="09156-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="09156-133">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="09156-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="09156-134">輸出</span><span class="sxs-lookup"><span data-stu-id="09156-134">OUTPUTS</span></span>

### <span data-ttu-id="09156-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="09156-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="09156-136">筆記</span><span class="sxs-lookup"><span data-stu-id="09156-136">NOTES</span></span>

## <span data-ttu-id="09156-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="09156-137">RELATED LINKS</span></span>

[<span data-ttu-id="09156-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="09156-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="09156-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="09156-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="09156-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="09156-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="09156-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="09156-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="09156-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


