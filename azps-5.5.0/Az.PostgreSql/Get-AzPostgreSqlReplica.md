---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128590"
---
# <span data-ttu-id="24526-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="24526-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="24526-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24526-102">SYNOPSIS</span></span>
<span data-ttu-id="24526-103">列出指定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="24526-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="24526-104">句法</span><span class="sxs-lookup"><span data-stu-id="24526-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="24526-105">說明</span><span class="sxs-lookup"><span data-stu-id="24526-105">DESCRIPTION</span></span>
<span data-ttu-id="24526-106">列出指定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="24526-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="24526-107">示例</span><span class="sxs-lookup"><span data-stu-id="24526-107">EXAMPLES</span></span>

### <span data-ttu-id="24526-108">範例1：依資源群組和伺服器名稱取得 PostgreSql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="24526-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="24526-109">這個 Cmdlet 會透過資源群組和伺服器名稱來取得 PostgreSql 伺服器複製。</span><span class="sxs-lookup"><span data-stu-id="24526-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="24526-110">參數</span><span class="sxs-lookup"><span data-stu-id="24526-110">PARAMETERS</span></span>

### <span data-ttu-id="24526-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24526-111">-DefaultProfile</span></span>
<span data-ttu-id="24526-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24526-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24526-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24526-113">-ResourceGroupName</span></span>
<span data-ttu-id="24526-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24526-114">The name of the resource group.</span></span>
<span data-ttu-id="24526-115">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="24526-115">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24526-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24526-116">-ServerName</span></span>
<span data-ttu-id="24526-117">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="24526-117">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24526-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24526-118">-SubscriptionId</span></span>
<span data-ttu-id="24526-119">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="24526-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24526-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24526-120">CommonParameters</span></span>
<span data-ttu-id="24526-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24526-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24526-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="24526-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24526-123">輸入</span><span class="sxs-lookup"><span data-stu-id="24526-123">INPUTS</span></span>

## <span data-ttu-id="24526-124">輸出</span><span class="sxs-lookup"><span data-stu-id="24526-124">OUTPUTS</span></span>

### <span data-ttu-id="24526-125">IServer （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="24526-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="24526-126">筆記</span><span class="sxs-lookup"><span data-stu-id="24526-126">NOTES</span></span>

<span data-ttu-id="24526-127">別名</span><span class="sxs-lookup"><span data-stu-id="24526-127">ALIASES</span></span>

## <span data-ttu-id="24526-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="24526-128">RELATED LINKS</span></span>

