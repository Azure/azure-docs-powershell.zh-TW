---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447186"
---
# <span data-ttu-id="f0591-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="f0591-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0591-102">SYNOPSIS</span></span>
<span data-ttu-id="f0591-103">修改 runbook。</span><span class="sxs-lookup"><span data-stu-id="f0591-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0591-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0591-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0591-105">說明</span><span class="sxs-lookup"><span data-stu-id="f0591-105">DESCRIPTION</span></span>
<span data-ttu-id="f0591-106">AzureRmAutomationRunbook Cmdlet 會修改 AP 中 Azure 自動化 runbook 的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="f0591-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="f0591-107">示例</span><span class="sxs-lookup"><span data-stu-id="f0591-107">EXAMPLES</span></span>

### <span data-ttu-id="f0591-108">範例1：針對 runbook 啟用詳細記錄</span><span class="sxs-lookup"><span data-stu-id="f0591-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f0591-109">這個命令會針對在名為 Contoso17 的 Azure 自動化帳戶中指定的 runbook 啟用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="f0591-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f0591-110">參數</span><span class="sxs-lookup"><span data-stu-id="f0591-110">PARAMETERS</span></span>

### <span data-ttu-id="f0591-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0591-111">-AutomationAccountName</span></span>
<span data-ttu-id="f0591-112">指定此 Cmdlet 修改 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f0591-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="f0591-113">-描述</span><span class="sxs-lookup"><span data-stu-id="f0591-113">-Description</span></span>
<span data-ttu-id="f0591-114">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="f0591-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="f0591-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="f0591-115">-LogProgress</span></span>
<span data-ttu-id="f0591-116">指定 runbook 是否要記錄進度。</span><span class="sxs-lookup"><span data-stu-id="f0591-116">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="f0591-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="f0591-117">-LogVerbose</span></span>
<span data-ttu-id="f0591-118">指定記錄是否包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f0591-118">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="f0591-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0591-119">-Name</span></span>
<span data-ttu-id="f0591-120">指定此 Cmdlet 修改的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="f0591-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f0591-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0591-121">-ResourceGroupName</span></span>
<span data-ttu-id="f0591-122">指定此 Cmdlet 修改 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0591-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="f0591-123">-標記</span><span class="sxs-lookup"><span data-stu-id="f0591-123">-Tags</span></span>
<span data-ttu-id="f0591-124">指定要取代已修改之 runbook 之目前標記的標記字典。</span><span class="sxs-lookup"><span data-stu-id="f0591-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

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

### <span data-ttu-id="f0591-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0591-125">-DefaultProfile</span></span>
<span data-ttu-id="f0591-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0591-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0591-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0591-127">CommonParameters</span></span>
<span data-ttu-id="f0591-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0591-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0591-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0591-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0591-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f0591-130">INPUTS</span></span>

## <span data-ttu-id="f0591-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f0591-131">OUTPUTS</span></span>

### <span data-ttu-id="f0591-132">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="f0591-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="f0591-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f0591-133">NOTES</span></span>

## <span data-ttu-id="f0591-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0591-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0591-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f0591-136">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f0591-137">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f0591-138">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f0591-139">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f0591-140">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f0591-141">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f0591-142">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f0591-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


