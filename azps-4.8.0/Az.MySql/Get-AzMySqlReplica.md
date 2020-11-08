---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129419"
---
# <span data-ttu-id="18c7b-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="18c7b-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="18c7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="18c7b-103">列出指定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="18c7b-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="18c7b-104">句法</span><span class="sxs-lookup"><span data-stu-id="18c7b-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="18c7b-105">說明</span><span class="sxs-lookup"><span data-stu-id="18c7b-105">DESCRIPTION</span></span>
<span data-ttu-id="18c7b-106">列出指定伺服器的所有複本。</span><span class="sxs-lookup"><span data-stu-id="18c7b-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="18c7b-107">示例</span><span class="sxs-lookup"><span data-stu-id="18c7b-107">EXAMPLES</span></span>

### <span data-ttu-id="18c7b-108">範例1：依資源群組和伺服器名稱取得 MySql 伺服器複本</span><span class="sxs-lookup"><span data-stu-id="18c7b-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="18c7b-109">這個 Cmdlet 透過資源群組和伺服器名稱來取得 MySql 伺服器複製。</span><span class="sxs-lookup"><span data-stu-id="18c7b-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="18c7b-110">參數</span><span class="sxs-lookup"><span data-stu-id="18c7b-110">PARAMETERS</span></span>

### <span data-ttu-id="18c7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c7b-111">-DefaultProfile</span></span>
<span data-ttu-id="18c7b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18c7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18c7b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c7b-113">-ResourceGroupName</span></span>
<span data-ttu-id="18c7b-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18c7b-114">The name of the resource group.</span></span>
<span data-ttu-id="18c7b-115">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="18c7b-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="18c7b-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="18c7b-116">-ServerName</span></span>
<span data-ttu-id="18c7b-117">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="18c7b-117">The name of the server.</span></span>

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

### <span data-ttu-id="18c7b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18c7b-118">-SubscriptionId</span></span>
<span data-ttu-id="18c7b-119">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="18c7b-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="18c7b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c7b-120">CommonParameters</span></span>
<span data-ttu-id="18c7b-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18c7b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c7b-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="18c7b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c7b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="18c7b-123">INPUTS</span></span>

## <span data-ttu-id="18c7b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="18c7b-124">OUTPUTS</span></span>

### <span data-ttu-id="18c7b-125">IServer 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="18c7b-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="18c7b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="18c7b-126">NOTES</span></span>

<span data-ttu-id="18c7b-127">別名</span><span class="sxs-lookup"><span data-stu-id="18c7b-127">ALIASES</span></span>

## <span data-ttu-id="18c7b-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="18c7b-128">RELATED LINKS</span></span>
