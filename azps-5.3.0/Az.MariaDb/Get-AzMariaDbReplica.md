---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438068"
---
# <span data-ttu-id="b4a6b-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="b4a6b-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="b4a6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a6b-103">列出指定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="b4a6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4a6b-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b4a6b-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="b4a6b-106">列出指定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="b4a6b-107">示例</span><span class="sxs-lookup"><span data-stu-id="b4a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="b4a6b-108">範例1：列出 MariaDB 下的所有複本資料庫</span><span class="sxs-lookup"><span data-stu-id="b4a6b-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="b4a6b-109">這個命令會列出 MariaDB 下的所有複本資料庫。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="b4a6b-110">參數</span><span class="sxs-lookup"><span data-stu-id="b4a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="b4a6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a6b-111">-DefaultProfile</span></span>
<span data-ttu-id="b4a6b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4a6b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a6b-113">-ResourceGroupName</span></span>
<span data-ttu-id="b4a6b-114">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b4a6b-115">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b4a6b-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4a6b-116">-ServerName</span></span>
<span data-ttu-id="b4a6b-117">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-117">The name of the server.</span></span>

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

### <span data-ttu-id="b4a6b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4a6b-118">-SubscriptionId</span></span>
<span data-ttu-id="b4a6b-119">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b4a6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a6b-120">CommonParameters</span></span>
<span data-ttu-id="b4a6b-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a6b-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a6b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b4a6b-123">INPUTS</span></span>

## <span data-ttu-id="b4a6b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b4a6b-124">OUTPUTS</span></span>

### <span data-ttu-id="b4a6b-125">IServer （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="b4a6b-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="b4a6b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b4a6b-126">NOTES</span></span>

<span data-ttu-id="b4a6b-127">別名</span><span class="sxs-lookup"><span data-stu-id="b4a6b-127">ALIASES</span></span>

## <span data-ttu-id="b4a6b-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4a6b-128">RELATED LINKS</span></span>

