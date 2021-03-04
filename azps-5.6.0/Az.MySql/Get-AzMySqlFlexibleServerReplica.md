---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 25444df39945527d1bc574283e397407e0218633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904633"
---
# <span data-ttu-id="7a2f1-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="7a2f1-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="7a2f1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7a2f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2f1-103">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="7a2f1-104">語法</span><span class="sxs-lookup"><span data-stu-id="7a2f1-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7a2f1-105">描述</span><span class="sxs-lookup"><span data-stu-id="7a2f1-105">DESCRIPTION</span></span>
<span data-ttu-id="7a2f1-106">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="7a2f1-107">例子</span><span class="sxs-lookup"><span data-stu-id="7a2f1-107">EXAMPLES</span></span>

### <span data-ttu-id="7a2f1-108">範例 1：根據資源群組和伺服器名稱取得 MySql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="7a2f1-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="7a2f1-109">此 Cmdlet 會根據資源群組和伺服器名稱，獲得 MySql 伺服器複本。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="7a2f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="7a2f1-110">PARAMETERS</span></span>

### <span data-ttu-id="7a2f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2f1-111">-DefaultProfile</span></span>
<span data-ttu-id="7a2f1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a2f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="7a2f1-114">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-114">The name of the resource group.</span></span>
<span data-ttu-id="7a2f1-115">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7a2f1-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a2f1-116">-ServerName</span></span>
<span data-ttu-id="7a2f1-117">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-117">The name of the server.</span></span>

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

### <span data-ttu-id="7a2f1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a2f1-118">-SubscriptionId</span></span>
<span data-ttu-id="7a2f1-119">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7a2f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2f1-120">CommonParameters</span></span>
<span data-ttu-id="7a2f1-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7a2f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2f1-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a2f1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2f1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7a2f1-123">INPUTS</span></span>

## <span data-ttu-id="7a2f1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7a2f1-124">OUTPUTS</span></span>

### <span data-ttu-id="7a2f1-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="7a2f1-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="7a2f1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7a2f1-126">NOTES</span></span>

<span data-ttu-id="7a2f1-127">別名</span><span class="sxs-lookup"><span data-stu-id="7a2f1-127">ALIASES</span></span>

## <span data-ttu-id="7a2f1-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a2f1-128">RELATED LINKS</span></span>

