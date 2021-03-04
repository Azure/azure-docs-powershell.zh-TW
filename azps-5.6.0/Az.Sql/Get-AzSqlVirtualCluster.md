---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: 624ca943d9adf7df105fae18a0a4a8ccad2b9b9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909937"
---
# <span data-ttu-id="a89c4-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="a89c4-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="a89c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a89c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a89c4-103">會返回 Azure SQL 虛擬組群相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a89c4-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="a89c4-104">語法</span><span class="sxs-lookup"><span data-stu-id="a89c4-104">SYNTAX</span></span>

### <span data-ttu-id="a89c4-105">GetVirtualClusterByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="a89c4-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a89c4-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a89c4-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a89c4-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="a89c4-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a89c4-108">描述</span><span class="sxs-lookup"><span data-stu-id="a89c4-108">DESCRIPTION</span></span>
<span data-ttu-id="a89c4-109">**Get-AzSqlVirtualCludlet Cmdlet** 會返回一或多個 Azure SQL 虛擬叢集相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a89c4-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="a89c4-110">指定虛擬組名，只查看該組的資訊。</span><span class="sxs-lookup"><span data-stu-id="a89c4-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="a89c4-111">例子</span><span class="sxs-lookup"><span data-stu-id="a89c4-111">EXAMPLES</span></span>

### <span data-ttu-id="a89c4-112">範例 1：取得指派給資源群組的所有虛擬群組</span><span class="sxs-lookup"><span data-stu-id="a89c4-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="a89c4-113">此命令會獲得所有指派給資源群組 ResourceGroup01 的虛擬群組相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a89c4-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a89c4-114">範例 2：取得特定虛擬組組的資訊</span><span class="sxs-lookup"><span data-stu-id="a89c4-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="a89c4-115">此命令會取得資源群組 ResourceGroup01 中虛擬叢集 VirtualCluster1 的資訊。</span><span class="sxs-lookup"><span data-stu-id="a89c4-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a89c4-116">參數</span><span class="sxs-lookup"><span data-stu-id="a89c4-116">PARAMETERS</span></span>

### <span data-ttu-id="a89c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89c4-117">-DefaultProfile</span></span>
<span data-ttu-id="a89c4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a89c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a89c4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a89c4-119">-Name</span></span>
<span data-ttu-id="a89c4-120">虛擬組名。</span><span class="sxs-lookup"><span data-stu-id="a89c4-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="a89c4-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a89c4-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89c4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a89c4-123">-ResourceId</span></span>
<span data-ttu-id="a89c4-124">要取得的實例物件資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a89c4-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89c4-125">CommonParameters</span></span>
<span data-ttu-id="a89c4-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a89c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89c4-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a89c4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89c4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a89c4-128">INPUTS</span></span>

### <span data-ttu-id="a89c4-129">沒有</span><span class="sxs-lookup"><span data-stu-id="a89c4-129">None</span></span>

## <span data-ttu-id="a89c4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a89c4-130">OUTPUTS</span></span>

### <span data-ttu-id="a89c4-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="a89c4-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="a89c4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a89c4-132">NOTES</span></span>

## <span data-ttu-id="a89c4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a89c4-133">RELATED LINKS</span></span>
