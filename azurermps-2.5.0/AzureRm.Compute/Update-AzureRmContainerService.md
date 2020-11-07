---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802522"
---
# <span data-ttu-id="275db-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="275db-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="275db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="275db-102">SYNOPSIS</span></span>
<span data-ttu-id="275db-103">更新容器服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="275db-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="275db-104">句法</span><span class="sxs-lookup"><span data-stu-id="275db-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275db-105">說明</span><span class="sxs-lookup"><span data-stu-id="275db-105">DESCRIPTION</span></span>
<span data-ttu-id="275db-106">**更新 AzureRmContainerService** Cmdlet 會更新容器服務的狀態，以符合服務的本機實例。</span><span class="sxs-lookup"><span data-stu-id="275db-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="275db-107">示例</span><span class="sxs-lookup"><span data-stu-id="275db-107">EXAMPLES</span></span>

### <span data-ttu-id="275db-108">範例1：更新容器服務</span><span class="sxs-lookup"><span data-stu-id="275db-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="275db-109">這個命令會使用 Get-AzureRmContainerService Cmdlet 來取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="275db-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="275db-110">命令會使用管線運算子，將該物件傳遞到 Remove-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="275db-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="275db-111">**移除-AzureRmContainerServiceAgentPoolProfile** 會移除名為 AgentPool01 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="275db-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="275db-112">命令會將結果傳遞到 Add-AzureRmContainerServiceAgentPoolProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="275db-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="275db-113">[ **載入 AzureRmContainerServiceAgentPoolProfile** ] 會新增具有名稱 AgentPool01 的設定檔，並具有指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="275db-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="275db-114">命令會將結果傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="275db-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="275db-115">目前的 Cmdlet 會更新容器服務，以反映此命令所做的變更。</span><span class="sxs-lookup"><span data-stu-id="275db-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="275db-116">參數</span><span class="sxs-lookup"><span data-stu-id="275db-116">PARAMETERS</span></span>

### <span data-ttu-id="275db-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="275db-117">-AsJob</span></span>
<span data-ttu-id="275db-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="275db-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275db-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="275db-119">-ContainerService</span></span>
<span data-ttu-id="275db-120">指定包含變更的本機 **ContainerService** 物件。</span><span class="sxs-lookup"><span data-stu-id="275db-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="275db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275db-121">-DefaultProfile</span></span>
<span data-ttu-id="275db-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="275db-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="275db-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="275db-123">-Name</span></span>
<span data-ttu-id="275db-124">指定此 Cmdlet 更新之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="275db-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="275db-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275db-125">-ResourceGroupName</span></span>
<span data-ttu-id="275db-126">指定此 Cmdlet 更新之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="275db-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="275db-127">-確認</span><span class="sxs-lookup"><span data-stu-id="275db-127">-Confirm</span></span>
<span data-ttu-id="275db-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="275db-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275db-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275db-129">-WhatIf</span></span>
<span data-ttu-id="275db-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="275db-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="275db-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="275db-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275db-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275db-132">CommonParameters</span></span>
<span data-ttu-id="275db-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="275db-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275db-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="275db-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275db-135">輸入</span><span class="sxs-lookup"><span data-stu-id="275db-135">INPUTS</span></span>

### <span data-ttu-id="275db-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="275db-136">ContainerService</span></span>
<span data-ttu-id="275db-137">形參 "ContainerService" 接受管線中 "ContainerService" 類型的值</span><span class="sxs-lookup"><span data-stu-id="275db-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="275db-138">輸出</span><span class="sxs-lookup"><span data-stu-id="275db-138">OUTPUTS</span></span>

### <span data-ttu-id="275db-139">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="275db-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="275db-140">筆記</span><span class="sxs-lookup"><span data-stu-id="275db-140">NOTES</span></span>

## <span data-ttu-id="275db-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="275db-141">RELATED LINKS</span></span>

[<span data-ttu-id="275db-142">附加 AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="275db-142">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="275db-143">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="275db-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="275db-144">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="275db-144">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="275db-145">移除-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="275db-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="275db-146">移除-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="275db-146">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


