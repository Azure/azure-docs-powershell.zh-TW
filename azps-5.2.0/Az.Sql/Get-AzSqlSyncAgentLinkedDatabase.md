---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280576"
---
# <span data-ttu-id="7f065-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="7f065-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="7f065-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f065-102">SYNOPSIS</span></span>
<span data-ttu-id="7f065-103">傳回同步處理代理程式所連結之 SQL Server 資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f065-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="7f065-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f065-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f065-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f065-105">DESCRIPTION</span></span>
<span data-ttu-id="7f065-106">**AzSqlSyncAgentLinkedDatabase** Cmdlet 會傳回同步處理代理程式所連結之 SQL Server 資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f065-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="7f065-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f065-107">EXAMPLES</span></span>

### <span data-ttu-id="7f065-108">範例1：取得 Azure SQL 同步處理代理程式的連結 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7f065-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="7f065-109">下列範例會傳回由 Azure SQL 同步處理代理程式連結的連結 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7f065-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="7f065-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f065-110">PARAMETERS</span></span>

### <span data-ttu-id="7f065-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f065-111">-DefaultProfile</span></span>
<span data-ttu-id="7f065-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7f065-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f065-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f065-113">-ResourceGroupName</span></span>
<span data-ttu-id="7f065-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f065-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f065-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f065-115">-ServerName</span></span>
<span data-ttu-id="7f065-116">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f065-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7f065-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="7f065-117">-SyncAgentName</span></span>
<span data-ttu-id="7f065-118">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="7f065-118">The sync agent name.</span></span>

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

### <span data-ttu-id="7f065-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f065-119">CommonParameters</span></span>
<span data-ttu-id="7f065-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f065-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f065-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7f065-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f065-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7f065-122">INPUTS</span></span>

### <span data-ttu-id="7f065-123">System.object</span><span class="sxs-lookup"><span data-stu-id="7f065-123">System.String</span></span>

## <span data-ttu-id="7f065-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7f065-124">OUTPUTS</span></span>

### <span data-ttu-id="7f065-125">AzureSqlSyncAgentLinkedDatabaseModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="7f065-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="7f065-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7f065-126">NOTES</span></span>

## <span data-ttu-id="7f065-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f065-127">RELATED LINKS</span></span>
