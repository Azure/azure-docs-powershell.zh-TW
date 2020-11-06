---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: 62acfacbafb50f85673b37e802b9d0b0eb4bf66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444672"
---
# <span data-ttu-id="05203-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="05203-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="05203-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05203-102">SYNOPSIS</span></span>
<span data-ttu-id="05203-103">更新容器服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="05203-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05203-104">句法</span><span class="sxs-lookup"><span data-stu-id="05203-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05203-105">說明</span><span class="sxs-lookup"><span data-stu-id="05203-105">DESCRIPTION</span></span>
<span data-ttu-id="05203-106">**更新 AzureRmContainerService** Cmdlet 會更新容器服務的狀態，以符合服務的本機實例。</span><span class="sxs-lookup"><span data-stu-id="05203-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="05203-107">示例</span><span class="sxs-lookup"><span data-stu-id="05203-107">EXAMPLES</span></span>

### <span data-ttu-id="05203-108">範例1：更新容器服務</span><span class="sxs-lookup"><span data-stu-id="05203-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="05203-109">這個命令會使用 Get-AzureRmContainerService Cmdlet 來取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="05203-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="05203-110">命令會使用管線運算子，將該物件傳遞到 Remove-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05203-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="05203-111">**移除-AzureRmContainerServiceAgentPoolProfile** 會移除名為 AgentPool01 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="05203-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="05203-112">命令會將結果傳遞到 Add-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05203-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="05203-113">[ **載入 AzureRmContainerServiceAgentPoolProfile** ] 會新增具有名稱 AgentPool01 的設定檔，並具有指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="05203-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="05203-114">命令會將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05203-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="05203-115">目前的 Cmdlet 會更新容器服務，以反映此命令所做的變更。</span><span class="sxs-lookup"><span data-stu-id="05203-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="05203-116">參數</span><span class="sxs-lookup"><span data-stu-id="05203-116">PARAMETERS</span></span>

### <span data-ttu-id="05203-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="05203-117">-ContainerService</span></span>
<span data-ttu-id="05203-118">指定包含變更的本機 **ContainerService** 物件。</span><span class="sxs-lookup"><span data-stu-id="05203-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05203-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="05203-119">-Name</span></span>
<span data-ttu-id="05203-120">指定此 Cmdlet 更新之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="05203-120">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05203-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05203-121">-ResourceGroupName</span></span>
<span data-ttu-id="05203-122">指定此 Cmdlet 更新之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="05203-122">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="05203-123">-確認</span><span class="sxs-lookup"><span data-stu-id="05203-123">-Confirm</span></span>
<span data-ttu-id="05203-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="05203-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05203-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05203-125">-WhatIf</span></span>
<span data-ttu-id="05203-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05203-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="05203-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05203-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05203-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05203-128">CommonParameters</span></span>
<span data-ttu-id="05203-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05203-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05203-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05203-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05203-131">輸入</span><span class="sxs-lookup"><span data-stu-id="05203-131">INPUTS</span></span>

### <span data-ttu-id="05203-132">所有</span><span class="sxs-lookup"><span data-stu-id="05203-132">None</span></span>
<span data-ttu-id="05203-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="05203-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05203-134">輸出</span><span class="sxs-lookup"><span data-stu-id="05203-134">OUTPUTS</span></span>

## <span data-ttu-id="05203-135">筆記</span><span class="sxs-lookup"><span data-stu-id="05203-135">NOTES</span></span>

## <span data-ttu-id="05203-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="05203-136">RELATED LINKS</span></span>

[<span data-ttu-id="05203-137">附加 AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="05203-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="05203-138">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="05203-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="05203-139">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="05203-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="05203-140">移除-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="05203-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="05203-141">移除-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="05203-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


