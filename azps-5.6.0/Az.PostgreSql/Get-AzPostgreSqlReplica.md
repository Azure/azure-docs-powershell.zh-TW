---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: c8fea3c7d0cfca227a69f83a76d73617d69106a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902354"
---
# <span data-ttu-id="a35f2-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="a35f2-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="a35f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a35f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a35f2-103">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="a35f2-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="a35f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="a35f2-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a35f2-105">描述</span><span class="sxs-lookup"><span data-stu-id="a35f2-105">DESCRIPTION</span></span>
<span data-ttu-id="a35f2-106">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="a35f2-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="a35f2-107">例子</span><span class="sxs-lookup"><span data-stu-id="a35f2-107">EXAMPLES</span></span>

### <span data-ttu-id="a35f2-108">範例 1：根據資源群組和伺服器名稱取得 PostgreSql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="a35f2-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a35f2-109">此 Cmdlet 會根據資源群組和伺服器名稱，獲得 PostgreSql 伺服器複本。</span><span class="sxs-lookup"><span data-stu-id="a35f2-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="a35f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a35f2-110">PARAMETERS</span></span>

### <span data-ttu-id="a35f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35f2-111">-DefaultProfile</span></span>
<span data-ttu-id="a35f2-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a35f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a35f2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a35f2-113">-ResourceGroupName</span></span>
<span data-ttu-id="a35f2-114">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a35f2-114">The name of the resource group.</span></span>
<span data-ttu-id="a35f2-115">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a35f2-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a35f2-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a35f2-116">-ServerName</span></span>
<span data-ttu-id="a35f2-117">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a35f2-117">The name of the server.</span></span>

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

### <span data-ttu-id="a35f2-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a35f2-118">-SubscriptionId</span></span>
<span data-ttu-id="a35f2-119">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a35f2-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a35f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35f2-120">CommonParameters</span></span>
<span data-ttu-id="a35f2-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a35f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35f2-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a35f2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35f2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a35f2-123">INPUTS</span></span>

## <span data-ttu-id="a35f2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a35f2-124">OUTPUTS</span></span>

### <span data-ttu-id="a35f2-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a35f2-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a35f2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a35f2-126">NOTES</span></span>

<span data-ttu-id="a35f2-127">別名</span><span class="sxs-lookup"><span data-stu-id="a35f2-127">ALIASES</span></span>

## <span data-ttu-id="a35f2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a35f2-128">RELATED LINKS</span></span>

