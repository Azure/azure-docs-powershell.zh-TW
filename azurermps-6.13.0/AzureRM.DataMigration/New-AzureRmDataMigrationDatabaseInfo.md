---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626414"
---
# <span data-ttu-id="23622-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="23622-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="23622-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23622-102">SYNOPSIS</span></span>
<span data-ttu-id="23622-103">建立 Azure Database 遷移服務的 DatabaseInfo 物件，該物件會指定要遷移的資料庫來源。</span><span class="sxs-lookup"><span data-stu-id="23622-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23622-104">句法</span><span class="sxs-lookup"><span data-stu-id="23622-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23622-105">說明</span><span class="sxs-lookup"><span data-stu-id="23622-105">DESCRIPTION</span></span>
<span data-ttu-id="23622-106">New-AzureRmDataMigrationDatabaseInfo Cmdlet 會建立 DatabaseInfo 物件，以指定要遷移的來源資料庫實例。</span><span class="sxs-lookup"><span data-stu-id="23622-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="23622-107">資料庫名稱是在輸入參數中取得。</span><span class="sxs-lookup"><span data-stu-id="23622-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="23622-108">示例</span><span class="sxs-lookup"><span data-stu-id="23622-108">EXAMPLES</span></span>

### <span data-ttu-id="23622-109">範例1</span><span class="sxs-lookup"><span data-stu-id="23622-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="23622-110">前面的範例會為源資料庫 **AdventureWorks2016** 建立新的 DatabaseInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="23622-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="23622-111">此腳本假設您已經登入您的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="23622-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="23622-112">您可以使用 Get-AzureSubscription Cmdlet 來確認您的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="23622-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="23622-113">參數</span><span class="sxs-lookup"><span data-stu-id="23622-113">PARAMETERS</span></span>

### <span data-ttu-id="23622-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23622-114">-DefaultProfile</span></span>
<span data-ttu-id="23622-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23622-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23622-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="23622-116">-SourceDatabaseName</span></span>
<span data-ttu-id="23622-117">來源資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="23622-117">Source Database Name.</span></span>

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

### <span data-ttu-id="23622-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23622-118">CommonParameters</span></span>
<span data-ttu-id="23622-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23622-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23622-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23622-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23622-121">輸入</span><span class="sxs-lookup"><span data-stu-id="23622-121">INPUTS</span></span>

### <span data-ttu-id="23622-122">所有</span><span class="sxs-lookup"><span data-stu-id="23622-122">None</span></span>

## <span data-ttu-id="23622-123">輸出</span><span class="sxs-lookup"><span data-stu-id="23622-123">OUTPUTS</span></span>

### <span data-ttu-id="23622-124">DatabaseInfo 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="23622-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="23622-125">筆記</span><span class="sxs-lookup"><span data-stu-id="23622-125">NOTES</span></span>

## <span data-ttu-id="23622-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="23622-126">RELATED LINKS</span></span>
