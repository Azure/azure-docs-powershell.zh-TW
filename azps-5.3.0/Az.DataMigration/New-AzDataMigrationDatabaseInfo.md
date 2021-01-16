---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289319"
---
# <span data-ttu-id="43959-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="43959-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="43959-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43959-102">SYNOPSIS</span></span>
<span data-ttu-id="43959-103">建立 Azure Database 遷移服務的 DatabaseInfo 物件，該物件會指定要遷移的資料庫來源。</span><span class="sxs-lookup"><span data-stu-id="43959-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="43959-104">句法</span><span class="sxs-lookup"><span data-stu-id="43959-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43959-105">說明</span><span class="sxs-lookup"><span data-stu-id="43959-105">DESCRIPTION</span></span>
<span data-ttu-id="43959-106">New-AzDataMigrationDatabaseInfo Cmdlet 會建立 DatabaseInfo 物件，以指定要遷移的來源資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="43959-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="43959-107">資料庫名稱是在輸入參數中取得。</span><span class="sxs-lookup"><span data-stu-id="43959-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="43959-108">示例</span><span class="sxs-lookup"><span data-stu-id="43959-108">EXAMPLES</span></span>

### <span data-ttu-id="43959-109">範例1</span><span class="sxs-lookup"><span data-stu-id="43959-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="43959-110">前面的範例會為源資料庫 **AdventureWorks2016** 建立新的 DatabaseInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="43959-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="43959-111">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="43959-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="43959-112">您可以使用 Get-AzSubscription Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="43959-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="43959-113">參數</span><span class="sxs-lookup"><span data-stu-id="43959-113">PARAMETERS</span></span>

### <span data-ttu-id="43959-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43959-114">-DefaultProfile</span></span>
<span data-ttu-id="43959-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43959-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43959-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="43959-116">-SourceDatabaseName</span></span>
<span data-ttu-id="43959-117">來源資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="43959-117">Source Database Name.</span></span>

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

### <span data-ttu-id="43959-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43959-118">CommonParameters</span></span>
<span data-ttu-id="43959-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43959-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43959-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43959-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43959-121">輸入</span><span class="sxs-lookup"><span data-stu-id="43959-121">INPUTS</span></span>

### <span data-ttu-id="43959-122">所有</span><span class="sxs-lookup"><span data-stu-id="43959-122">None</span></span>

## <span data-ttu-id="43959-123">輸出</span><span class="sxs-lookup"><span data-stu-id="43959-123">OUTPUTS</span></span>

### <span data-ttu-id="43959-124">DatabaseInfo 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="43959-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="43959-125">筆記</span><span class="sxs-lookup"><span data-stu-id="43959-125">NOTES</span></span>

## <span data-ttu-id="43959-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="43959-126">RELATED LINKS</span></span>
