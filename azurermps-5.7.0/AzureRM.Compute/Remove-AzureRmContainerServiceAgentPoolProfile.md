---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623611"
---
# <span data-ttu-id="be14a-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="be14a-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="be14a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be14a-102">SYNOPSIS</span></span>
<span data-ttu-id="be14a-103">從容器服務移除代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="be14a-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be14a-104">句法</span><span class="sxs-lookup"><span data-stu-id="be14a-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be14a-105">說明</span><span class="sxs-lookup"><span data-stu-id="be14a-105">DESCRIPTION</span></span>
<span data-ttu-id="be14a-106">**AzureRmContainerServiceAgentPoolProfile** Cmdlet 會從容器服務中移除代理程式組件池設定檔。</span><span class="sxs-lookup"><span data-stu-id="be14a-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="be14a-107">示例</span><span class="sxs-lookup"><span data-stu-id="be14a-107">EXAMPLES</span></span>

### <span data-ttu-id="be14a-108">範例1：從容器服務移除設定檔</span><span class="sxs-lookup"><span data-stu-id="be14a-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="be14a-109">第一個命令會使用 Get-AzureRmContainerService Cmdlet 來取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="be14a-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="be14a-110">該命令會將服務儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="be14a-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="be14a-111">第二個命令會從 $Container 的容器服務中移除名為 AgentPool01 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="be14a-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="be14a-112">參數</span><span class="sxs-lookup"><span data-stu-id="be14a-112">PARAMETERS</span></span>

### <span data-ttu-id="be14a-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="be14a-113">-ContainerService</span></span>
<span data-ttu-id="be14a-114">指定此 Cmdlet 從中移除代理程式組件設定檔的容器服務物件。</span><span class="sxs-lookup"><span data-stu-id="be14a-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be14a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="be14a-115">-Name</span></span>
<span data-ttu-id="be14a-116">指定此 Cmdlet 移除的代理池設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="be14a-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="be14a-117">-確認</span><span class="sxs-lookup"><span data-stu-id="be14a-117">-Confirm</span></span>
<span data-ttu-id="be14a-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be14a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be14a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be14a-119">-WhatIf</span></span>
<span data-ttu-id="be14a-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be14a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be14a-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be14a-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be14a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be14a-122">CommonParameters</span></span>
<span data-ttu-id="be14a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be14a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be14a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be14a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be14a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="be14a-125">INPUTS</span></span>

### <span data-ttu-id="be14a-126">所有</span><span class="sxs-lookup"><span data-stu-id="be14a-126">None</span></span>
<span data-ttu-id="be14a-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="be14a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be14a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="be14a-128">OUTPUTS</span></span>

## <span data-ttu-id="be14a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="be14a-129">NOTES</span></span>

## <span data-ttu-id="be14a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="be14a-130">RELATED LINKS</span></span>

[<span data-ttu-id="be14a-131">附加 AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="be14a-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="be14a-132">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="be14a-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


