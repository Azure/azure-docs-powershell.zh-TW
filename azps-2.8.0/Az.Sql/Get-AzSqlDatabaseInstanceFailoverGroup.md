---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: dbb0cb56c50025e6b257d801957b1a75479220f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792549"
---
# <span data-ttu-id="6e0d1-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6e0d1-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="6e0d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0d1-103">取得或列出實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="6e0d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e0d1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e0d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="6e0d1-105">DESCRIPTION</span></span>
<span data-ttu-id="6e0d1-106">取得特定的實例容錯移轉群組，或列出使用者訂閱下區域中的實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="6e0d1-107">實例容錯移轉群組中的任何一個區域，都可以用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="6e0d1-108">傳回的值將反映該區域中與實例容錯移轉群組相關的受管理實例狀態。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="6e0d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="6e0d1-109">EXAMPLES</span></span>

### <span data-ttu-id="6e0d1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6e0d1-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
    ResourceGroupName                     : rg
    Location                              : East US
    Name                                  : fg
    PartnerResourceGroupName              : rg
    PartnerRegion                         : West US
    PrimaryManagedInstanceName            : managedInstance1
    PartnerManagedInstanceName            : managedInstance2
    ReplicationRole                       : Primary
    ReplicationState                      : CATCH_UP
    ReadWriteFailoverPolicy               : Automatic
    FailoverWithDataLossGracePeriodHours  : 1
    ReadOnlyFailoverPolicy                : Disabled
    Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
}
```

<span data-ttu-id="6e0d1-111">列出區域中的所有容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="6e0d1-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="6e0d1-112">範例2</span><span class="sxs-lookup"><span data-stu-id="6e0d1-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="6e0d1-113">取得特定的實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="6e0d1-114">參數</span><span class="sxs-lookup"><span data-stu-id="6e0d1-114">PARAMETERS</span></span>

### <span data-ttu-id="6e0d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0d1-115">-DefaultProfile</span></span>
<span data-ttu-id="6e0d1-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e0d1-117">-位置</span><span class="sxs-lookup"><span data-stu-id="6e0d1-117">-Location</span></span>
<span data-ttu-id="6e0d1-118">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0d1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e0d1-119">-Name</span></span>
<span data-ttu-id="6e0d1-120">要檢索之實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0d1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e0d1-121">-ResourceGroupName</span></span>
<span data-ttu-id="6e0d1-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0d1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0d1-123">CommonParameters</span></span>
<span data-ttu-id="6e0d1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0d1-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e0d1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0d1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6e0d1-126">INPUTS</span></span>

### <span data-ttu-id="6e0d1-127">System.object</span><span class="sxs-lookup"><span data-stu-id="6e0d1-127">System.String</span></span>

## <span data-ttu-id="6e0d1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6e0d1-128">OUTPUTS</span></span>

### <span data-ttu-id="6e0d1-129">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="6e0d1-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="6e0d1-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6e0d1-130">NOTES</span></span>

## <span data-ttu-id="6e0d1-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e0d1-131">RELATED LINKS</span></span>
