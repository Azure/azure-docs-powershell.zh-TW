---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 2b8ddc8b15ca9fa7322de231f9688548c4073708
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917617"
---
# <span data-ttu-id="7e4f6-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e4f6-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="7e4f6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7e4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4f6-103">獲取或列出實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="7e4f6-104">語法</span><span class="sxs-lookup"><span data-stu-id="7e4f6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e4f6-105">描述</span><span class="sxs-lookup"><span data-stu-id="7e4f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7e4f6-106">在使用者訂閱下的一個地區中，獲得特定的實例容錯移轉群組或列出實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="7e4f6-107">實例容錯移轉群組中的任一區域都可以用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="7e4f6-108">所返回的值會反映該區域中與實例容錯移轉群組有關之受管理實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="7e4f6-109">例子</span><span class="sxs-lookup"><span data-stu-id="7e4f6-109">EXAMPLES</span></span>

### <span data-ttu-id="7e4f6-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="7e4f6-110">Example 1</span></span>
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

<span data-ttu-id="7e4f6-111">列出地區內的所有容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="7e4f6-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="7e4f6-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="7e4f6-112">Example 2</span></span>
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

<span data-ttu-id="7e4f6-113">取得特定的實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="7e4f6-114">參數</span><span class="sxs-lookup"><span data-stu-id="7e4f6-114">PARAMETERS</span></span>

### <span data-ttu-id="7e4f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4f6-115">-DefaultProfile</span></span>
<span data-ttu-id="7e4f6-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e4f6-117">-位置</span><span class="sxs-lookup"><span data-stu-id="7e4f6-117">-Location</span></span>
<span data-ttu-id="7e4f6-118">要從其中取回實例容錯移轉群組的當地地區名稱。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4f6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e4f6-119">-Name</span></span>
<span data-ttu-id="7e4f6-120">要取回的實例容錯移轉組名。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e4f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e4f6-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4f6-123">CommonParameters</span></span>
<span data-ttu-id="7e4f6-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7e4f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4f6-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e4f6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4f6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7e4f6-126">INPUTS</span></span>

### <span data-ttu-id="7e4f6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7e4f6-127">System.String</span></span>

## <span data-ttu-id="7e4f6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7e4f6-128">OUTPUTS</span></span>

### <span data-ttu-id="7e4f6-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7e4f6-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="7e4f6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7e4f6-130">NOTES</span></span>

## <span data-ttu-id="7e4f6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e4f6-131">RELATED LINKS</span></span>
