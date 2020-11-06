---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 29d85284261b5885c90bcd50b1d54a580b53e10d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614269"
---
# <span data-ttu-id="a58f5-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="a58f5-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="a58f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a58f5-102">SYNOPSIS</span></span>

## <span data-ttu-id="a58f5-103">句法</span><span class="sxs-lookup"><span data-stu-id="a58f5-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a58f5-104">說明</span><span class="sxs-lookup"><span data-stu-id="a58f5-104">DESCRIPTION</span></span>
<span data-ttu-id="a58f5-105">**新的-AzWebAppDatabaseBackupSetting** Cmdlet 會建立新的 Azure Web App 備份設定。</span><span class="sxs-lookup"><span data-stu-id="a58f5-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="a58f5-106">示例</span><span class="sxs-lookup"><span data-stu-id="a58f5-106">EXAMPLES</span></span>

### <span data-ttu-id="a58f5-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="a58f5-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="a58f5-108">針對資源群組預設-Web-WestUS 中的指定 app ContosoWebApp，建立 (連接字串) 類型 SqlAzure 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="a58f5-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a58f5-109">參數</span><span class="sxs-lookup"><span data-stu-id="a58f5-109">PARAMETERS</span></span>

### <span data-ttu-id="a58f5-110">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a58f5-110">-ConnectionString</span></span>
<span data-ttu-id="a58f5-111">連接字串</span><span class="sxs-lookup"><span data-stu-id="a58f5-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58f5-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="a58f5-112">-ConnectionStringName</span></span>
<span data-ttu-id="a58f5-113">連接字串名稱</span><span class="sxs-lookup"><span data-stu-id="a58f5-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58f5-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="a58f5-114">-DatabaseType</span></span>
<span data-ttu-id="a58f5-115">資料庫類型 ( 例如「SqlAzure」或「MySql」 ) </span><span class="sxs-lookup"><span data-stu-id="a58f5-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="a58f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58f5-116">-DefaultProfile</span></span>
<span data-ttu-id="a58f5-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a58f5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a58f5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a58f5-118">-Name</span></span>
<span data-ttu-id="a58f5-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a58f5-119">WebApp Name</span></span>

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

### <span data-ttu-id="a58f5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58f5-120">CommonParameters</span></span>
<span data-ttu-id="a58f5-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a58f5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58f5-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a58f5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58f5-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a58f5-123">INPUTS</span></span>

### <span data-ttu-id="a58f5-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a58f5-124">System.String</span></span>

## <span data-ttu-id="a58f5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a58f5-125">OUTPUTS</span></span>

### <span data-ttu-id="a58f5-126">DatabaseBackupSetting 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="a58f5-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="a58f5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a58f5-127">NOTES</span></span>

## <span data-ttu-id="a58f5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a58f5-128">RELATED LINKS</span></span>
