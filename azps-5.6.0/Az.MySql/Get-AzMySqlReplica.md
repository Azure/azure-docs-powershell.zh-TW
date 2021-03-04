---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: d4579ec17d870c1f002ce40309aa580226ff143d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904630"
---
# <span data-ttu-id="f79f0-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="f79f0-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="f79f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f79f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f79f0-103">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="f79f0-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="f79f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f79f0-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f79f0-105">描述</span><span class="sxs-lookup"><span data-stu-id="f79f0-105">DESCRIPTION</span></span>
<span data-ttu-id="f79f0-106">列出給定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="f79f0-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="f79f0-107">例子</span><span class="sxs-lookup"><span data-stu-id="f79f0-107">EXAMPLES</span></span>

### <span data-ttu-id="f79f0-108">範例 1：根據資源群組和伺服器名稱取得 MySql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="f79f0-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="f79f0-109">此 Cmdlet 會根據資源群組和伺服器名稱，獲得 MySql 伺服器複本。</span><span class="sxs-lookup"><span data-stu-id="f79f0-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="f79f0-110">參數</span><span class="sxs-lookup"><span data-stu-id="f79f0-110">PARAMETERS</span></span>

### <span data-ttu-id="f79f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79f0-111">-DefaultProfile</span></span>
<span data-ttu-id="f79f0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f79f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f79f0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79f0-113">-ResourceGroupName</span></span>
<span data-ttu-id="f79f0-114">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f79f0-114">The name of the resource group.</span></span>
<span data-ttu-id="f79f0-115">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f79f0-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f79f0-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f79f0-116">-ServerName</span></span>
<span data-ttu-id="f79f0-117">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f79f0-117">The name of the server.</span></span>

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

### <span data-ttu-id="f79f0-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f79f0-118">-SubscriptionId</span></span>
<span data-ttu-id="f79f0-119">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f79f0-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f79f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79f0-120">CommonParameters</span></span>
<span data-ttu-id="f79f0-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f79f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79f0-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f79f0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79f0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f79f0-123">INPUTS</span></span>

## <span data-ttu-id="f79f0-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f79f0-124">OUTPUTS</span></span>

### <span data-ttu-id="f79f0-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="f79f0-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f79f0-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f79f0-126">NOTES</span></span>

<span data-ttu-id="f79f0-127">別名</span><span class="sxs-lookup"><span data-stu-id="f79f0-127">ALIASES</span></span>

## <span data-ttu-id="f79f0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f79f0-128">RELATED LINKS</span></span>

