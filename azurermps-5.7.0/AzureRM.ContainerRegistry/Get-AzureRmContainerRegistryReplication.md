---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: db03414e9cebe4c1593013a928b8a66d9b70bd91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447847"
---
# <span data-ttu-id="0edd6-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0edd6-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="0edd6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0edd6-102">SYNOPSIS</span></span>
<span data-ttu-id="0edd6-103">取得容器註冊表的複製。</span><span class="sxs-lookup"><span data-stu-id="0edd6-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0edd6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0edd6-104">SYNTAX</span></span>

### <span data-ttu-id="0edd6-105">ListReplicationByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0edd6-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edd6-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0edd6-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edd6-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0edd6-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edd6-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0edd6-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0edd6-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0edd6-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0edd6-110">說明</span><span class="sxs-lookup"><span data-stu-id="0edd6-110">DESCRIPTION</span></span>
<span data-ttu-id="0edd6-111">Get-AzureRmContainerRegistryReplication Cmdlet 會取得容器登錄的指定複製，或容器註冊的所有複製。</span><span class="sxs-lookup"><span data-stu-id="0edd6-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="0edd6-112">示例</span><span class="sxs-lookup"><span data-stu-id="0edd6-112">EXAMPLES</span></span>

### <span data-ttu-id="0edd6-113">範例1：取得容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="0edd6-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="0edd6-114">取得容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="0edd6-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="0edd6-115">範例2：取得容器註冊的所有複製</span><span class="sxs-lookup"><span data-stu-id="0edd6-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="0edd6-116">取得容器註冊的所有複製</span><span class="sxs-lookup"><span data-stu-id="0edd6-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="0edd6-117">參數</span><span class="sxs-lookup"><span data-stu-id="0edd6-117">PARAMETERS</span></span>

### <span data-ttu-id="0edd6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0edd6-118">-DefaultProfile</span></span>
<span data-ttu-id="0edd6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0edd6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0edd6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0edd6-120">-Name</span></span>
<span data-ttu-id="0edd6-121">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="0edd6-121">Container Registry Replication Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0edd6-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="0edd6-122">-Registry</span></span>
<span data-ttu-id="0edd6-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="0edd6-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0edd6-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0edd6-124">-RegistryName</span></span>
<span data-ttu-id="0edd6-125">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="0edd6-125">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0edd6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0edd6-126">-ResourceGroupName</span></span>
<span data-ttu-id="0edd6-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0edd6-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0edd6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0edd6-128">-ResourceId</span></span>
<span data-ttu-id="0edd6-129">容器登錄複製資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0edd6-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="0edd6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0edd6-130">CommonParameters</span></span>
<span data-ttu-id="0edd6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0edd6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0edd6-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0edd6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0edd6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0edd6-133">INPUTS</span></span>

### <span data-ttu-id="0edd6-134">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0edd6-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="0edd6-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0edd6-135">System.String</span></span>

## <span data-ttu-id="0edd6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="0edd6-136">OUTPUTS</span></span>

### <span data-ttu-id="0edd6-137">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0edd6-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="0edd6-138">ContainerRegistry. PSContainerRegistryReplication []</span><span class="sxs-lookup"><span data-stu-id="0edd6-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication[]</span></span>

## <span data-ttu-id="0edd6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0edd6-139">NOTES</span></span>

## <span data-ttu-id="0edd6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0edd6-140">RELATED LINKS</span></span>

[<span data-ttu-id="0edd6-141">新-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0edd6-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="0edd6-142">移除-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0edd6-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
