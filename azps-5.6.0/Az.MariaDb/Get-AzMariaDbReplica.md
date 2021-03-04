---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: c6fef537c3a0cc01bd2de01e00b69c1a69f81e3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906586"
---
# <span data-ttu-id="dbd31-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="dbd31-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="dbd31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dbd31-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd31-103">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="dbd31-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="dbd31-104">語法</span><span class="sxs-lookup"><span data-stu-id="dbd31-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dbd31-105">描述</span><span class="sxs-lookup"><span data-stu-id="dbd31-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd31-106">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="dbd31-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="dbd31-107">例子</span><span class="sxs-lookup"><span data-stu-id="dbd31-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd31-108">範例 1：在 MariaDB 下列出所有複本 DB</span><span class="sxs-lookup"><span data-stu-id="dbd31-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="dbd31-109">此命令會列出 MariaDB 下的所有複本 DB。</span><span class="sxs-lookup"><span data-stu-id="dbd31-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="dbd31-110">參數</span><span class="sxs-lookup"><span data-stu-id="dbd31-110">PARAMETERS</span></span>

### <span data-ttu-id="dbd31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd31-111">-DefaultProfile</span></span>
<span data-ttu-id="dbd31-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbd31-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd31-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd31-113">-ResourceGroupName</span></span>
<span data-ttu-id="dbd31-114">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="dbd31-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dbd31-115">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="dbd31-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dbd31-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dbd31-116">-ServerName</span></span>
<span data-ttu-id="dbd31-117">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dbd31-117">The name of the server.</span></span>

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

### <span data-ttu-id="dbd31-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dbd31-118">-SubscriptionId</span></span>
<span data-ttu-id="dbd31-119">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbd31-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="dbd31-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd31-120">CommonParameters</span></span>
<span data-ttu-id="dbd31-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dbd31-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd31-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbd31-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd31-123">輸入</span><span class="sxs-lookup"><span data-stu-id="dbd31-123">INPUTS</span></span>

## <span data-ttu-id="dbd31-124">輸出</span><span class="sxs-lookup"><span data-stu-id="dbd31-124">OUTPUTS</span></span>

### <span data-ttu-id="dbd31-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="dbd31-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="dbd31-126">筆記</span><span class="sxs-lookup"><span data-stu-id="dbd31-126">NOTES</span></span>

<span data-ttu-id="dbd31-127">別名</span><span class="sxs-lookup"><span data-stu-id="dbd31-127">ALIASES</span></span>

## <span data-ttu-id="dbd31-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbd31-128">RELATED LINKS</span></span>

