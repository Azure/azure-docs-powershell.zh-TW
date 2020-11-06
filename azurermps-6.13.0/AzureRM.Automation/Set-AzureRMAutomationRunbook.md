---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 26f3214cf98e43a805aab99eb3ad1b92f289b2bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448481"
---
# <span data-ttu-id="e5193-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="e5193-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5193-102">SYNOPSIS</span></span>
<span data-ttu-id="e5193-103">修改 runbook。</span><span class="sxs-lookup"><span data-stu-id="e5193-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5193-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5193-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5193-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5193-105">DESCRIPTION</span></span>
<span data-ttu-id="e5193-106">AzureRmAutomationRunbook Cmdlet 會修改 AP 中 Azure 自動化 runbook 的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="e5193-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="e5193-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5193-107">EXAMPLES</span></span>

### <span data-ttu-id="e5193-108">範例1：針對 runbook 啟用詳細記錄</span><span class="sxs-lookup"><span data-stu-id="e5193-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e5193-109">這個命令會針對在名為 Contoso17 的 Azure 自動化帳戶中指定的 runbook 啟用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="e5193-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e5193-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5193-110">PARAMETERS</span></span>

### <span data-ttu-id="e5193-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5193-111">-AutomationAccountName</span></span>
<span data-ttu-id="e5193-112">指定此 Cmdlet 修改 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e5193-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="e5193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5193-113">-DefaultProfile</span></span>
<span data-ttu-id="e5193-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5193-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5193-115">-描述</span><span class="sxs-lookup"><span data-stu-id="e5193-115">-Description</span></span>
<span data-ttu-id="e5193-116">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="e5193-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="e5193-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="e5193-117">-LogProgress</span></span>
<span data-ttu-id="e5193-118">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="e5193-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="e5193-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="e5193-119">-LogVerbose</span></span>
<span data-ttu-id="e5193-120">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e5193-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="e5193-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5193-121">-Name</span></span>
<span data-ttu-id="e5193-122">指定此 Cmdlet 修改的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="e5193-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e5193-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5193-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5193-124">指定此 Cmdlet 修改 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5193-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="e5193-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5193-125">-Tag</span></span>
<span data-ttu-id="e5193-126">[Runbook] 標記。</span><span class="sxs-lookup"><span data-stu-id="e5193-126">The runbook tags.</span></span>

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

### <span data-ttu-id="e5193-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5193-127">CommonParameters</span></span>
<span data-ttu-id="e5193-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5193-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5193-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5193-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5193-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e5193-130">INPUTS</span></span>

### <span data-ttu-id="e5193-131">System.object</span><span class="sxs-lookup"><span data-stu-id="e5193-131">System.String</span></span>

### <span data-ttu-id="e5193-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e5193-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="e5193-133">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e5193-133">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e5193-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e5193-134">OUTPUTS</span></span>

### <span data-ttu-id="e5193-135">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="e5193-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="e5193-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e5193-136">NOTES</span></span>

## <span data-ttu-id="e5193-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5193-137">RELATED LINKS</span></span>

[<span data-ttu-id="e5193-138">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-138">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e5193-139">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-139">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e5193-140">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-140">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e5193-141">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e5193-142">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-142">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e5193-143">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-143">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e5193-144">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-144">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="e5193-145">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e5193-145">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


