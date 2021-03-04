---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: b27aee4c665dd2725bfd8643cb12ca005a5c4e1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917546"
---
# <span data-ttu-id="19dfb-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="19dfb-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="19dfb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="19dfb-103">會返回由同步處理代理程式連結的 SQL Server 資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="19dfb-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="19dfb-104">語法</span><span class="sxs-lookup"><span data-stu-id="19dfb-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19dfb-105">描述</span><span class="sxs-lookup"><span data-stu-id="19dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="19dfb-106">**Get-AzSqlSyncAgentLinkedDatabase** Cmdlet 會傳送同步處理代理程式所連結的 SQL Server 資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="19dfb-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="19dfb-107">例子</span><span class="sxs-lookup"><span data-stu-id="19dfb-107">EXAMPLES</span></span>

### <span data-ttu-id="19dfb-108">範例 1：取得 Azure SQL 同步處理代理程式的連結 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="19dfb-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="19dfb-109">下列範例會返回由 Azure SQL 同步處理代理程式連結的連結 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="19dfb-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="19dfb-110">參數</span><span class="sxs-lookup"><span data-stu-id="19dfb-110">PARAMETERS</span></span>

### <span data-ttu-id="19dfb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dfb-111">-DefaultProfile</span></span>
<span data-ttu-id="19dfb-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="19dfb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19dfb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19dfb-113">-ResourceGroupName</span></span>
<span data-ttu-id="19dfb-114">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="19dfb-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dfb-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="19dfb-115">-ServerName</span></span>
<span data-ttu-id="19dfb-116">同步處理代理程式位於 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="19dfb-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dfb-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="19dfb-117">-SyncAgentName</span></span>
<span data-ttu-id="19dfb-118">同步代理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="19dfb-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dfb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dfb-119">CommonParameters</span></span>
<span data-ttu-id="19dfb-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19dfb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dfb-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19dfb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dfb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="19dfb-122">INPUTS</span></span>

### <span data-ttu-id="19dfb-123">System.String</span><span class="sxs-lookup"><span data-stu-id="19dfb-123">System.String</span></span>

## <span data-ttu-id="19dfb-124">輸出</span><span class="sxs-lookup"><span data-stu-id="19dfb-124">OUTPUTS</span></span>

### <span data-ttu-id="19dfb-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="19dfb-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="19dfb-126">筆記</span><span class="sxs-lookup"><span data-stu-id="19dfb-126">NOTES</span></span>

## <span data-ttu-id="19dfb-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="19dfb-127">RELATED LINKS</span></span>
