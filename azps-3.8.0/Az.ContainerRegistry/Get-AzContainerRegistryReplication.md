---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797350"
---
# <span data-ttu-id="e432c-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e432c-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="e432c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e432c-102">SYNOPSIS</span></span>
<span data-ttu-id="e432c-103">取得容器註冊表的複製。</span><span class="sxs-lookup"><span data-stu-id="e432c-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="e432c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e432c-104">SYNTAX</span></span>

### <span data-ttu-id="e432c-105">ListReplicationByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e432c-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e432c-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e432c-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e432c-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e432c-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e432c-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e432c-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e432c-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e432c-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e432c-110">說明</span><span class="sxs-lookup"><span data-stu-id="e432c-110">DESCRIPTION</span></span>
<span data-ttu-id="e432c-111">Get-AzContainerRegistryReplication Cmdlet 會取得容器登錄的指定複製，或容器註冊的所有複製。</span><span class="sxs-lookup"><span data-stu-id="e432c-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="e432c-112">示例</span><span class="sxs-lookup"><span data-stu-id="e432c-112">EXAMPLES</span></span>

### <span data-ttu-id="e432c-113">範例1：取得容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="e432c-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e432c-114">取得容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="e432c-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="e432c-115">範例2：取得容器註冊的所有複製</span><span class="sxs-lookup"><span data-stu-id="e432c-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e432c-116">取得容器註冊的所有複製</span><span class="sxs-lookup"><span data-stu-id="e432c-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="e432c-117">參數</span><span class="sxs-lookup"><span data-stu-id="e432c-117">PARAMETERS</span></span>

### <span data-ttu-id="e432c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e432c-118">-DefaultProfile</span></span>
<span data-ttu-id="e432c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e432c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e432c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e432c-120">-Name</span></span>
<span data-ttu-id="e432c-121">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="e432c-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e432c-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="e432c-122">-Registry</span></span>
<span data-ttu-id="e432c-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="e432c-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e432c-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e432c-124">-RegistryName</span></span>
<span data-ttu-id="e432c-125">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="e432c-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e432c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e432c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e432c-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e432c-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e432c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e432c-128">-ResourceId</span></span>
<span data-ttu-id="e432c-129">容器登錄複製資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e432c-129">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e432c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e432c-130">CommonParameters</span></span>
<span data-ttu-id="e432c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e432c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e432c-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e432c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e432c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e432c-133">INPUTS</span></span>

### <span data-ttu-id="e432c-134">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e432c-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="e432c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e432c-135">System.String</span></span>

## <span data-ttu-id="e432c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e432c-136">OUTPUTS</span></span>

### <span data-ttu-id="e432c-137">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e432c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="e432c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e432c-138">NOTES</span></span>

## <span data-ttu-id="e432c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e432c-139">RELATED LINKS</span></span>

[<span data-ttu-id="e432c-140">新-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e432c-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="e432c-141">移除-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e432c-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)