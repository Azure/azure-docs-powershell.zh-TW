---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279545"
---
# <span data-ttu-id="a5183-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a5183-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="a5183-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5183-102">SYNOPSIS</span></span>
<span data-ttu-id="a5183-103">取得或列出實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a5183-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="a5183-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5183-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5183-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5183-105">DESCRIPTION</span></span>
<span data-ttu-id="a5183-106">取得特定的實例容錯移轉群組，或列出使用者訂閱下區域中的實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a5183-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="a5183-107">實例容錯移轉群組中的任何一個區域，都可以用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="a5183-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="a5183-108">傳回的值將反映該區域中與實例容錯移轉群組相關的受管理實例狀態。</span><span class="sxs-lookup"><span data-stu-id="a5183-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="a5183-109">示例</span><span class="sxs-lookup"><span data-stu-id="a5183-109">EXAMPLES</span></span>

### <span data-ttu-id="a5183-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a5183-110">Example 1</span></span>
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

<span data-ttu-id="a5183-111">列出區域中的所有容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="a5183-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="a5183-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a5183-112">Example 2</span></span>
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

<span data-ttu-id="a5183-113">取得特定的實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="a5183-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="a5183-114">參數</span><span class="sxs-lookup"><span data-stu-id="a5183-114">PARAMETERS</span></span>

### <span data-ttu-id="a5183-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5183-115">-DefaultProfile</span></span>
<span data-ttu-id="a5183-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5183-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5183-117">-位置</span><span class="sxs-lookup"><span data-stu-id="a5183-117">-Location</span></span>
<span data-ttu-id="a5183-118">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a5183-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="a5183-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5183-119">-Name</span></span>
<span data-ttu-id="a5183-120">要檢索之實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5183-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="a5183-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5183-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5183-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5183-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5183-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5183-123">CommonParameters</span></span>
<span data-ttu-id="a5183-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5183-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5183-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5183-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5183-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a5183-126">INPUTS</span></span>

### <span data-ttu-id="a5183-127">System.object</span><span class="sxs-lookup"><span data-stu-id="a5183-127">System.String</span></span>

## <span data-ttu-id="a5183-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a5183-128">OUTPUTS</span></span>

### <span data-ttu-id="a5183-129">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="a5183-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="a5183-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a5183-130">NOTES</span></span>

## <span data-ttu-id="a5183-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5183-131">RELATED LINKS</span></span>
