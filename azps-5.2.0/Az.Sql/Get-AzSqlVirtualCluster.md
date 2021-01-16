---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283719"
---
# <span data-ttu-id="cee61-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="cee61-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="cee61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cee61-102">SYNOPSIS</span></span>
<span data-ttu-id="cee61-103">傳回有關 Azure SQL 虛擬叢集的資訊。</span><span class="sxs-lookup"><span data-stu-id="cee61-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="cee61-104">句法</span><span class="sxs-lookup"><span data-stu-id="cee61-104">SYNTAX</span></span>

### <span data-ttu-id="cee61-105">GetVirtualClusterByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="cee61-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cee61-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cee61-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cee61-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="cee61-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cee61-108">說明</span><span class="sxs-lookup"><span data-stu-id="cee61-108">DESCRIPTION</span></span>
<span data-ttu-id="cee61-109">**AzSqlVirtualCluster** Cmdlet 會傳回一或多個 Azure SQL 虛擬叢集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cee61-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="cee61-110">指定虛擬叢集的名稱，只查看該群集的資訊。</span><span class="sxs-lookup"><span data-stu-id="cee61-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="cee61-111">示例</span><span class="sxs-lookup"><span data-stu-id="cee61-111">EXAMPLES</span></span>

### <span data-ttu-id="cee61-112">範例1：取得指派給資源群組的所有虛擬叢集</span><span class="sxs-lookup"><span data-stu-id="cee61-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="cee61-113">這個命令會取得指派給資源群組 ResourceGroup01 的所有虛擬叢集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cee61-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="cee61-114">範例2：取得特定虛擬叢集的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cee61-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="cee61-115">這個命令會在資源群組 ResourceGroup01 中取得虛擬叢集 VirtualCluster1 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cee61-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="cee61-116">參數</span><span class="sxs-lookup"><span data-stu-id="cee61-116">PARAMETERS</span></span>

### <span data-ttu-id="cee61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee61-117">-DefaultProfile</span></span>
<span data-ttu-id="cee61-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cee61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cee61-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cee61-119">-Name</span></span>
<span data-ttu-id="cee61-120">虛擬叢集的名稱。</span><span class="sxs-lookup"><span data-stu-id="cee61-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="cee61-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee61-121">-ResourceGroupName</span></span>
<span data-ttu-id="cee61-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cee61-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="cee61-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cee61-123">-ResourceId</span></span>
<span data-ttu-id="cee61-124">要取得之實例物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cee61-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="cee61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee61-125">CommonParameters</span></span>
<span data-ttu-id="cee61-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cee61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee61-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cee61-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee61-128">輸入</span><span class="sxs-lookup"><span data-stu-id="cee61-128">INPUTS</span></span>

### <span data-ttu-id="cee61-129">所有</span><span class="sxs-lookup"><span data-stu-id="cee61-129">None</span></span>

## <span data-ttu-id="cee61-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cee61-130">OUTPUTS</span></span>

### <span data-ttu-id="cee61-131">AzureSqlVirtualClusterModel 中的 [VirtualCluster]</span><span class="sxs-lookup"><span data-stu-id="cee61-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="cee61-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cee61-132">NOTES</span></span>

## <span data-ttu-id="cee61-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cee61-133">RELATED LINKS</span></span>
