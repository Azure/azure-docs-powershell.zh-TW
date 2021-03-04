---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 3054c6ed8083d1108c853ab188903cc3b2ebd380
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915557"
---
# <span data-ttu-id="5de83-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5de83-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="5de83-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5de83-102">SYNOPSIS</span></span>
<span data-ttu-id="5de83-103">複製容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="5de83-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="5de83-104">語法</span><span class="sxs-lookup"><span data-stu-id="5de83-104">SYNTAX</span></span>

### <span data-ttu-id="5de83-105">ListReplicationByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5de83-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5de83-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5de83-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5de83-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5de83-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5de83-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5de83-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5de83-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5de83-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5de83-110">描述</span><span class="sxs-lookup"><span data-stu-id="5de83-110">DESCRIPTION</span></span>
<span data-ttu-id="5de83-111">Cmdlet Get-AzContainerRegistryReplication容器註冊表的指定複製，或容器註冊表的所有複製。</span><span class="sxs-lookup"><span data-stu-id="5de83-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="5de83-112">例子</span><span class="sxs-lookup"><span data-stu-id="5de83-112">EXAMPLES</span></span>

### <span data-ttu-id="5de83-113">範例 1：獲取容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="5de83-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="5de83-114">獲得容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="5de83-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="5de83-115">範例 2：獲取容器註冊表的所有複製</span><span class="sxs-lookup"><span data-stu-id="5de83-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="5de83-116">獲得容器註冊表的所有複製</span><span class="sxs-lookup"><span data-stu-id="5de83-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="5de83-117">參數</span><span class="sxs-lookup"><span data-stu-id="5de83-117">PARAMETERS</span></span>

### <span data-ttu-id="5de83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de83-118">-DefaultProfile</span></span>
<span data-ttu-id="5de83-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5de83-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5de83-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5de83-120">-Name</span></span>
<span data-ttu-id="5de83-121">容器註冊表複製名稱。</span><span class="sxs-lookup"><span data-stu-id="5de83-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="5de83-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="5de83-122">-Registry</span></span>
<span data-ttu-id="5de83-123">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="5de83-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="5de83-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5de83-124">-RegistryName</span></span>
<span data-ttu-id="5de83-125">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="5de83-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="5de83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de83-126">-ResourceGroupName</span></span>
<span data-ttu-id="5de83-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5de83-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="5de83-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5de83-128">-ResourceId</span></span>
<span data-ttu-id="5de83-129">容器登錄複製資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5de83-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="5de83-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de83-130">CommonParameters</span></span>
<span data-ttu-id="5de83-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5de83-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de83-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5de83-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de83-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5de83-133">INPUTS</span></span>

### <span data-ttu-id="5de83-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5de83-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="5de83-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5de83-135">System.String</span></span>

## <span data-ttu-id="5de83-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5de83-136">OUTPUTS</span></span>

### <span data-ttu-id="5de83-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5de83-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="5de83-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5de83-138">NOTES</span></span>

## <span data-ttu-id="5de83-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5de83-139">RELATED LINKS</span></span>

[<span data-ttu-id="5de83-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5de83-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="5de83-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5de83-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)