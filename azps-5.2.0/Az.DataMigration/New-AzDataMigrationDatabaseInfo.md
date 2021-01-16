---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274540"
---
# <span data-ttu-id="ee70b-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="ee70b-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="ee70b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee70b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee70b-103">建立 Azure Database 遷移服務的 DatabaseInfo 物件，該物件會指定要遷移的資料庫來源。</span><span class="sxs-lookup"><span data-stu-id="ee70b-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="ee70b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee70b-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee70b-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee70b-105">DESCRIPTION</span></span>
<span data-ttu-id="ee70b-106">New-AzDataMigrationDatabaseInfo Cmdlet 會建立 DatabaseInfo 物件，以指定要遷移的來源資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="ee70b-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="ee70b-107">資料庫名稱是在輸入參數中取得。</span><span class="sxs-lookup"><span data-stu-id="ee70b-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="ee70b-108">示例</span><span class="sxs-lookup"><span data-stu-id="ee70b-108">EXAMPLES</span></span>

### <span data-ttu-id="ee70b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ee70b-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="ee70b-110">前面的範例會為源資料庫 **AdventureWorks2016** 建立新的 DatabaseInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="ee70b-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="ee70b-111">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="ee70b-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="ee70b-112">您可以使用 Get-AzSubscription Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="ee70b-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="ee70b-113">參數</span><span class="sxs-lookup"><span data-stu-id="ee70b-113">PARAMETERS</span></span>

### <span data-ttu-id="ee70b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee70b-114">-DefaultProfile</span></span>
<span data-ttu-id="ee70b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee70b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee70b-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee70b-116">-SourceDatabaseName</span></span>
<span data-ttu-id="ee70b-117">來源資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ee70b-117">Source Database Name.</span></span>

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

### <span data-ttu-id="ee70b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee70b-118">CommonParameters</span></span>
<span data-ttu-id="ee70b-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee70b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee70b-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee70b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee70b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ee70b-121">INPUTS</span></span>

### <span data-ttu-id="ee70b-122">所有</span><span class="sxs-lookup"><span data-stu-id="ee70b-122">None</span></span>

## <span data-ttu-id="ee70b-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ee70b-123">OUTPUTS</span></span>

### <span data-ttu-id="ee70b-124">DatabaseInfo 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="ee70b-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="ee70b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ee70b-125">NOTES</span></span>

## <span data-ttu-id="ee70b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee70b-126">RELATED LINKS</span></span>
