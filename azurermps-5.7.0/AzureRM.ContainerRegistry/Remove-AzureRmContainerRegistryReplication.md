---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624186"
---
# <span data-ttu-id="9d4fe-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="9d4fe-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="9d4fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4fe-103">移除容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d4fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d4fe-104">SYNTAX</span></span>

### <span data-ttu-id="9d4fe-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9d4fe-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d4fe-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d4fe-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d4fe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d4fe-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d4fe-108">說明</span><span class="sxs-lookup"><span data-stu-id="9d4fe-108">DESCRIPTION</span></span>
<span data-ttu-id="9d4fe-109">Remove-AzureRmContainerRegistryReplication Cmdlet 會移除容器註冊複本。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="9d4fe-110">示例</span><span class="sxs-lookup"><span data-stu-id="9d4fe-110">EXAMPLES</span></span>

### <span data-ttu-id="9d4fe-111">範例1：移除容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="9d4fe-112">移除容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="9d4fe-113">參數</span><span class="sxs-lookup"><span data-stu-id="9d4fe-113">PARAMETERS</span></span>

### <span data-ttu-id="9d4fe-114">-確認</span><span class="sxs-lookup"><span data-stu-id="9d4fe-114">-Confirm</span></span>
<span data-ttu-id="9d4fe-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d4fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4fe-116">-DefaultProfile</span></span>
<span data-ttu-id="9d4fe-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d4fe-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d4fe-118">-Name</span></span>
<span data-ttu-id="9d4fe-119">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="9d4fe-120">預設為位置名稱。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4fe-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="9d4fe-121">-RegistryName</span></span>
<span data-ttu-id="9d4fe-122">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4fe-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="9d4fe-123">-Replicatoin</span></span>
<span data-ttu-id="9d4fe-124">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d4fe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d4fe-125">-ResourceGroupName</span></span>
<span data-ttu-id="9d4fe-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d4fe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d4fe-127">-ResourceId</span></span>
<span data-ttu-id="9d4fe-128">容器登錄複製資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9d4fe-128">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d4fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d4fe-129">-WhatIf</span></span>
<span data-ttu-id="9d4fe-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d4fe-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d4fe-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d4fe-132">-PassThru</span></span>
<span data-ttu-id="9d4fe-133">表示如果移除成功，此 Cmdlet 會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="9d4fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4fe-134">CommonParameters</span></span>
<span data-ttu-id="9d4fe-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4fe-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d4fe-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4fe-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9d4fe-137">INPUTS</span></span>

### <span data-ttu-id="9d4fe-138">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9d4fe-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="9d4fe-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9d4fe-139">System.String</span></span>

## <span data-ttu-id="9d4fe-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9d4fe-140">OUTPUTS</span></span>

### <span data-ttu-id="9d4fe-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9d4fe-141">System.Object</span></span>

## <span data-ttu-id="9d4fe-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9d4fe-142">NOTES</span></span>

## <span data-ttu-id="9d4fe-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d4fe-143">RELATED LINKS</span></span>

[<span data-ttu-id="9d4fe-144">新-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="9d4fe-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="9d4fe-145">AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="9d4fe-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

