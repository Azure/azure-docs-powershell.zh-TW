---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: fe39df8c93a504b6a7c3ba9db4a3de18096dd820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446639"
---
# <span data-ttu-id="14209-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="14209-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="14209-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14209-102">SYNOPSIS</span></span>
<span data-ttu-id="14209-103">傳回同步處理代理程式所連結之 SQL Server 資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14209-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14209-104">句法</span><span class="sxs-lookup"><span data-stu-id="14209-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14209-105">說明</span><span class="sxs-lookup"><span data-stu-id="14209-105">DESCRIPTION</span></span>
<span data-ttu-id="14209-106">**AzureRmSqlSyncAgentLinkedDatabases** Cmdlet 會傳回同步處理代理程式所連結之 SQL Server 資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14209-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="14209-107">示例</span><span class="sxs-lookup"><span data-stu-id="14209-107">EXAMPLES</span></span>

### <span data-ttu-id="14209-108">範例1：取得 Azure SQL 同步處理代理程式的連結 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="14209-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="14209-109">這個命令會傳回由 Azure SQL 同步處理代理程式連結的連結 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="14209-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="14209-110">參數</span><span class="sxs-lookup"><span data-stu-id="14209-110">PARAMETERS</span></span>

### <span data-ttu-id="14209-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14209-111">-ResourceGroupName</span></span>
<span data-ttu-id="14209-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14209-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="14209-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="14209-113">-ServerName</span></span>
<span data-ttu-id="14209-114">同步處理常式所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="14209-114">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="14209-115">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="14209-115">-SyncAgentName</span></span>
<span data-ttu-id="14209-116">同步處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="14209-116">The sync agent name.</span></span>

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

### <span data-ttu-id="14209-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14209-117">-DefaultProfile</span></span>
<span data-ttu-id="14209-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14209-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14209-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14209-119">CommonParameters</span></span>
<span data-ttu-id="14209-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14209-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14209-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14209-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14209-122">輸入</span><span class="sxs-lookup"><span data-stu-id="14209-122">INPUTS</span></span>

## <span data-ttu-id="14209-123">輸出</span><span class="sxs-lookup"><span data-stu-id="14209-123">OUTPUTS</span></span>

### <span data-ttu-id="14209-124">AzureSqlSyncAgentLinkedDatabaseModel 中的 [DataSync]</span><span class="sxs-lookup"><span data-stu-id="14209-124">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="14209-125">筆記</span><span class="sxs-lookup"><span data-stu-id="14209-125">NOTES</span></span>

## <span data-ttu-id="14209-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="14209-126">RELATED LINKS</span></span>

