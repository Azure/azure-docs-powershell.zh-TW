---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794978"
---
# <span data-ttu-id="1b1ae-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1b1ae-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="1b1ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b1ae-102">SYNOPSIS</span></span>

## <span data-ttu-id="1b1ae-103">句法</span><span class="sxs-lookup"><span data-stu-id="1b1ae-103">SYNTAX</span></span>

### <span data-ttu-id="1b1ae-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1b1ae-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="1b1ae-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1b1ae-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="1b1ae-106">說明</span><span class="sxs-lookup"><span data-stu-id="1b1ae-106">DESCRIPTION</span></span>
<span data-ttu-id="1b1ae-107">**新的-AzWebAppBackup** Cmdlet 會建立 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="1b1ae-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="1b1ae-108">示例</span><span class="sxs-lookup"><span data-stu-id="1b1ae-108">EXAMPLES</span></span>

### <span data-ttu-id="1b1ae-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="1b1ae-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="1b1ae-110">在「資源群組預設-Web-WestUS」中建立指定 app ContosoWebApp 的備份 https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="1b1ae-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="1b1ae-111">參數</span><span class="sxs-lookup"><span data-stu-id="1b1ae-111">PARAMETERS</span></span>

### <span data-ttu-id="1b1ae-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="1b1ae-112">-BackupName</span></span>
<span data-ttu-id="1b1ae-113">備份名稱</span><span class="sxs-lookup"><span data-stu-id="1b1ae-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-114">-資料庫</span><span class="sxs-lookup"><span data-stu-id="1b1ae-114">-Databases</span></span>
<span data-ttu-id="1b1ae-115">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="1b1ae-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1ae-116">-DefaultProfile</span></span>
<span data-ttu-id="1b1ae-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b1ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b1ae-118">-Name</span></span>
<span data-ttu-id="1b1ae-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="1b1ae-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1ae-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b1ae-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1b1ae-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-122">-槽</span><span class="sxs-lookup"><span data-stu-id="1b1ae-122">-Slot</span></span>
<span data-ttu-id="1b1ae-123">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="1b1ae-123">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="1b1ae-124">-StorageAccountUrl</span></span>
<span data-ttu-id="1b1ae-125">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="1b1ae-125">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1b1ae-126">-WebApp</span></span>
<span data-ttu-id="1b1ae-127">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="1b1ae-127">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b1ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1ae-128">CommonParameters</span></span>
<span data-ttu-id="1b1ae-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b1ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1ae-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b1ae-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1ae-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1b1ae-131">INPUTS</span></span>

### <span data-ttu-id="1b1ae-132">網站地圖</span><span class="sxs-lookup"><span data-stu-id="1b1ae-132">Site</span></span>
<span data-ttu-id="1b1ae-133">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1b1ae-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1b1ae-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1b1ae-134">OUTPUTS</span></span>

### <span data-ttu-id="1b1ae-135">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="1b1ae-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="1b1ae-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1b1ae-136">NOTES</span></span>

## <span data-ttu-id="1b1ae-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b1ae-137">RELATED LINKS</span></span>

