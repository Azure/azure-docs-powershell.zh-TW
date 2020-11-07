---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623423"
---
# <span data-ttu-id="78a66-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="78a66-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="78a66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78a66-102">SYNOPSIS</span></span>
<span data-ttu-id="78a66-103">取得容器註冊表的複製。</span><span class="sxs-lookup"><span data-stu-id="78a66-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78a66-104">句法</span><span class="sxs-lookup"><span data-stu-id="78a66-104">SYNTAX</span></span>

### <span data-ttu-id="78a66-105">ListReplicationByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="78a66-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a66-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a66-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a66-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a66-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a66-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a66-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a66-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a66-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78a66-110">說明</span><span class="sxs-lookup"><span data-stu-id="78a66-110">DESCRIPTION</span></span>
<span data-ttu-id="78a66-111">Get-AzureRmContainerRegistryReplication Cmdlet 會取得容器登錄的指定複製，或容器註冊的所有複製。</span><span class="sxs-lookup"><span data-stu-id="78a66-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="78a66-112">示例</span><span class="sxs-lookup"><span data-stu-id="78a66-112">EXAMPLES</span></span>

### <span data-ttu-id="78a66-113">範例1：取得容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="78a66-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="78a66-114">取得容器註冊表的指定複製</span><span class="sxs-lookup"><span data-stu-id="78a66-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="78a66-115">範例2：取得容器註冊的所有複製</span><span class="sxs-lookup"><span data-stu-id="78a66-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="78a66-116">取得容器註冊的所有複製</span><span class="sxs-lookup"><span data-stu-id="78a66-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="78a66-117">參數</span><span class="sxs-lookup"><span data-stu-id="78a66-117">PARAMETERS</span></span>

### <span data-ttu-id="78a66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a66-118">-DefaultProfile</span></span>
<span data-ttu-id="78a66-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78a66-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a66-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="78a66-120">-Name</span></span>
<span data-ttu-id="78a66-121">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="78a66-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="78a66-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="78a66-122">-Registry</span></span>
<span data-ttu-id="78a66-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="78a66-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="78a66-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="78a66-124">-RegistryName</span></span>
<span data-ttu-id="78a66-125">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="78a66-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="78a66-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a66-126">-ResourceGroupName</span></span>
<span data-ttu-id="78a66-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="78a66-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="78a66-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78a66-128">-ResourceId</span></span>
<span data-ttu-id="78a66-129">容器登錄複製資源識別碼</span><span class="sxs-lookup"><span data-stu-id="78a66-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="78a66-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a66-130">CommonParameters</span></span>
<span data-ttu-id="78a66-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78a66-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a66-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78a66-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a66-133">輸入</span><span class="sxs-lookup"><span data-stu-id="78a66-133">INPUTS</span></span>

### <span data-ttu-id="78a66-134">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="78a66-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="78a66-135">參數： Registry (ByValue) </span><span class="sxs-lookup"><span data-stu-id="78a66-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="78a66-136">System.object</span><span class="sxs-lookup"><span data-stu-id="78a66-136">System.String</span></span>

## <span data-ttu-id="78a66-137">輸出</span><span class="sxs-lookup"><span data-stu-id="78a66-137">OUTPUTS</span></span>

### <span data-ttu-id="78a66-138">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="78a66-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="78a66-139">筆記</span><span class="sxs-lookup"><span data-stu-id="78a66-139">NOTES</span></span>

## <span data-ttu-id="78a66-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="78a66-140">RELATED LINKS</span></span>

[<span data-ttu-id="78a66-141">新-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="78a66-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="78a66-142">移除-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="78a66-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
