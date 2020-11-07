---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956675"
---
# <span data-ttu-id="b2bb2-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="b2bb2-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="b2bb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2bb2-102">SYNOPSIS</span></span>

## <span data-ttu-id="b2bb2-103">句法</span><span class="sxs-lookup"><span data-stu-id="b2bb2-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2bb2-104">說明</span><span class="sxs-lookup"><span data-stu-id="b2bb2-104">DESCRIPTION</span></span>
<span data-ttu-id="b2bb2-105">**新的-AzWebAppDatabaseBackupSetting** Cmdlet 會建立新的 Azure Web App 備份設定。</span><span class="sxs-lookup"><span data-stu-id="b2bb2-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="b2bb2-106">示例</span><span class="sxs-lookup"><span data-stu-id="b2bb2-106">EXAMPLES</span></span>

### <span data-ttu-id="b2bb2-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="b2bb2-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="b2bb2-108">針對資源群組預設-Web-WestUS 中的指定 app ContosoWebApp，建立 (連接字串) 類型 SqlAzure 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="b2bb2-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b2bb2-109">參數</span><span class="sxs-lookup"><span data-stu-id="b2bb2-109">PARAMETERS</span></span>

### <span data-ttu-id="b2bb2-110">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b2bb2-110">-ConnectionString</span></span>
<span data-ttu-id="b2bb2-111">連接字串</span><span class="sxs-lookup"><span data-stu-id="b2bb2-111">Connection String</span></span>

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

### <span data-ttu-id="b2bb2-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="b2bb2-112">-ConnectionStringName</span></span>
<span data-ttu-id="b2bb2-113">連接字串名稱</span><span class="sxs-lookup"><span data-stu-id="b2bb2-113">Connection String Name</span></span>

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

### <span data-ttu-id="b2bb2-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="b2bb2-114">-DatabaseType</span></span>
<span data-ttu-id="b2bb2-115">資料庫類型 ( 例如「SqlAzure」或「MySql」 ) </span><span class="sxs-lookup"><span data-stu-id="b2bb2-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="b2bb2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bb2-116">-DefaultProfile</span></span>
<span data-ttu-id="b2bb2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2bb2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2bb2-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2bb2-118">-Name</span></span>
<span data-ttu-id="b2bb2-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="b2bb2-119">WebApp Name</span></span>

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

### <span data-ttu-id="b2bb2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bb2-120">CommonParameters</span></span>
<span data-ttu-id="b2bb2-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2bb2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bb2-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2bb2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bb2-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b2bb2-123">INPUTS</span></span>

### <span data-ttu-id="b2bb2-124">System.object</span><span class="sxs-lookup"><span data-stu-id="b2bb2-124">System.String</span></span>

## <span data-ttu-id="b2bb2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b2bb2-125">OUTPUTS</span></span>

### <span data-ttu-id="b2bb2-126">DatabaseBackupSetting 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="b2bb2-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="b2bb2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b2bb2-127">NOTES</span></span>

## <span data-ttu-id="b2bb2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2bb2-128">RELATED LINKS</span></span>
