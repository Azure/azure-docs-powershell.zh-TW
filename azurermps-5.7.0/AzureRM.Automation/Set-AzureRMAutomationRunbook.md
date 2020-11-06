---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46c77e1538c367e38220a022bf3b84e796dd0ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453199"
---
# <span data-ttu-id="778a8-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="778a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="778a8-102">SYNOPSIS</span></span>
<span data-ttu-id="778a8-103">修改 runbook。</span><span class="sxs-lookup"><span data-stu-id="778a8-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="778a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="778a8-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="778a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="778a8-105">DESCRIPTION</span></span>
<span data-ttu-id="778a8-106">AzureRmAutomationRunbook Cmdlet 會修改 AP 中 Azure 自動化 runbook 的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="778a8-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="778a8-107">示例</span><span class="sxs-lookup"><span data-stu-id="778a8-107">EXAMPLES</span></span>

### <span data-ttu-id="778a8-108">範例1：針對 runbook 啟用詳細記錄</span><span class="sxs-lookup"><span data-stu-id="778a8-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="778a8-109">這個命令會針對在名為 Contoso17 的 Azure 自動化帳戶中指定的 runbook 啟用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="778a8-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="778a8-110">參數</span><span class="sxs-lookup"><span data-stu-id="778a8-110">PARAMETERS</span></span>

### <span data-ttu-id="778a8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="778a8-111">-AutomationAccountName</span></span>
<span data-ttu-id="778a8-112">指定此 Cmdlet 修改 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="778a8-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778a8-113">-DefaultProfile</span></span>
<span data-ttu-id="778a8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="778a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-115">-描述</span><span class="sxs-lookup"><span data-stu-id="778a8-115">-Description</span></span>
<span data-ttu-id="778a8-116">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="778a8-116">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="778a8-117">-LogProgress</span></span>
<span data-ttu-id="778a8-118">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="778a8-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="778a8-119">-LogVerbose</span></span>
<span data-ttu-id="778a8-120">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="778a8-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="778a8-121">-Name</span></span>
<span data-ttu-id="778a8-122">指定此 Cmdlet 修改的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="778a8-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778a8-123">-ResourceGroupName</span></span>
<span data-ttu-id="778a8-124">指定此 Cmdlet 修改 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="778a8-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="778a8-125">-Tag</span></span>
<span data-ttu-id="778a8-126">[Runbook] 標記。</span><span class="sxs-lookup"><span data-stu-id="778a8-126">The runbook tags.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778a8-127">CommonParameters</span></span>
<span data-ttu-id="778a8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="778a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778a8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="778a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778a8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="778a8-130">INPUTS</span></span>

### <span data-ttu-id="778a8-131">所有</span><span class="sxs-lookup"><span data-stu-id="778a8-131">None</span></span>
<span data-ttu-id="778a8-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="778a8-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="778a8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="778a8-133">OUTPUTS</span></span>

### <span data-ttu-id="778a8-134">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="778a8-134">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="778a8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="778a8-135">NOTES</span></span>

## <span data-ttu-id="778a8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="778a8-136">RELATED LINKS</span></span>

[<span data-ttu-id="778a8-137">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-137">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="778a8-138">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-138">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="778a8-139">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-139">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="778a8-140">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-140">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="778a8-141">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="778a8-142">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-142">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="778a8-143">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-143">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="778a8-144">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="778a8-144">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


