---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: 2152835d997532b490a6be16bf329831071f2f87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905578"
---
# <span data-ttu-id="d9bc0-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d9bc0-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="d9bc0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bc0-103">為 Azure 資料庫移移服務建立 DatabaseInfo 物件，指定要移移的資料庫來源。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="d9bc0-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9bc0-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9bc0-105">描述</span><span class="sxs-lookup"><span data-stu-id="d9bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bc0-106">此New-AzDataMigrationDatabaseInfo Cmdlet 會建立 DatabaseInfo 物件，指定要移轉的來源資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="d9bc0-107">資料庫名稱會以輸入參數方式輸入。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="d9bc0-108">例子</span><span class="sxs-lookup"><span data-stu-id="d9bc0-108">EXAMPLES</span></span>

### <span data-ttu-id="d9bc0-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="d9bc0-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="d9bc0-110">上述範例會為源資料庫 **AdventureWorks2016** 建立一個新的 DatabaseInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="d9bc0-111">此腳本假設您已經登入 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="d9bc0-112">您可以使用 Cmdlet Get-AzSubscription登入狀態。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="d9bc0-113">參數</span><span class="sxs-lookup"><span data-stu-id="d9bc0-113">PARAMETERS</span></span>

### <span data-ttu-id="d9bc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bc0-114">-DefaultProfile</span></span>
<span data-ttu-id="d9bc0-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bc0-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9bc0-116">-SourceDatabaseName</span></span>
<span data-ttu-id="d9bc0-117">來源資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9bc0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bc0-118">CommonParameters</span></span>
<span data-ttu-id="d9bc0-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bc0-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d9bc0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bc0-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d9bc0-121">INPUTS</span></span>

### <span data-ttu-id="d9bc0-122">沒有</span><span class="sxs-lookup"><span data-stu-id="d9bc0-122">None</span></span>

## <span data-ttu-id="d9bc0-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d9bc0-123">OUTPUTS</span></span>

### <span data-ttu-id="d9bc0-124">Microsoft.Azure.management.DataMigration.models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d9bc0-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="d9bc0-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d9bc0-125">NOTES</span></span>

## <span data-ttu-id="d9bc0-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9bc0-126">RELATED LINKS</span></span>
