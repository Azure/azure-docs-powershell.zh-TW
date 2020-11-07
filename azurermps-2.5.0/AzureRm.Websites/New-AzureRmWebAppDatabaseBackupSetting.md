---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
ms.openlocfilehash: f44b6f370b1431a5baf1a0686b4e893653327227
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802177"
---
# <span data-ttu-id="3287f-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="3287f-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="3287f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3287f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3287f-103">句法</span><span class="sxs-lookup"><span data-stu-id="3287f-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3287f-104">說明</span><span class="sxs-lookup"><span data-stu-id="3287f-104">DESCRIPTION</span></span>
<span data-ttu-id="3287f-105">**新的-AzureRmWebAppDatabaseBackupSetting** Cmdlet 會建立新的 Azure Web App 備份設定。</span><span class="sxs-lookup"><span data-stu-id="3287f-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="3287f-106">示例</span><span class="sxs-lookup"><span data-stu-id="3287f-106">EXAMPLES</span></span>

### <span data-ttu-id="3287f-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="3287f-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="3287f-108">針對資源群組預設-Web-WestUS 中的指定 app ContosoWebApp，建立 (連接字串) 類型 SqlAzure 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="3287f-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3287f-109">參數</span><span class="sxs-lookup"><span data-stu-id="3287f-109">PARAMETERS</span></span>

### <span data-ttu-id="3287f-110">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3287f-110">-ConnectionString</span></span>
<span data-ttu-id="3287f-111">連接字串</span><span class="sxs-lookup"><span data-stu-id="3287f-111">Connection String</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3287f-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="3287f-112">-ConnectionStringName</span></span>
<span data-ttu-id="3287f-113">連接字串名稱</span><span class="sxs-lookup"><span data-stu-id="3287f-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3287f-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="3287f-114">-DatabaseType</span></span>
<span data-ttu-id="3287f-115">資料庫類型 ( 例如「SqlAzure」或「MySql」 ) </span><span class="sxs-lookup"><span data-stu-id="3287f-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3287f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3287f-116">-DefaultProfile</span></span>
<span data-ttu-id="3287f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3287f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3287f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3287f-118">-Name</span></span>
<span data-ttu-id="3287f-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="3287f-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3287f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3287f-120">CommonParameters</span></span>
<span data-ttu-id="3287f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3287f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3287f-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3287f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3287f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="3287f-123">INPUTS</span></span>

### <span data-ttu-id="3287f-124">所有</span><span class="sxs-lookup"><span data-stu-id="3287f-124">None</span></span>
<span data-ttu-id="3287f-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3287f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3287f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="3287f-126">OUTPUTS</span></span>

### <span data-ttu-id="3287f-127">DatabaseBackupSetting 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="3287f-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="3287f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="3287f-128">NOTES</span></span>

## <span data-ttu-id="3287f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="3287f-129">RELATED LINKS</span></span>

