---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 7245697cab6184aa5fc2f7c292875f96cf3de3fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800621"
---
# <span data-ttu-id="fdb56-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="fdb56-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="fdb56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdb56-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb56-103">句法</span><span class="sxs-lookup"><span data-stu-id="fdb56-103">SYNTAX</span></span>

### <span data-ttu-id="fdb56-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fdb56-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="fdb56-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fdb56-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="fdb56-106">說明</span><span class="sxs-lookup"><span data-stu-id="fdb56-106">DESCRIPTION</span></span>
<span data-ttu-id="fdb56-107">**新的-AzureRmWebAppBackup** Cmdlet 會建立 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="fdb56-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="fdb56-108">示例</span><span class="sxs-lookup"><span data-stu-id="fdb56-108">EXAMPLES</span></span>

### <span data-ttu-id="fdb56-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="fdb56-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="fdb56-110">在「資源群組預設-Web-WestUS」中建立指定 app ContosoWebApp 的備份 https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="fdb56-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="fdb56-111">參數</span><span class="sxs-lookup"><span data-stu-id="fdb56-111">PARAMETERS</span></span>

### <span data-ttu-id="fdb56-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="fdb56-112">-BackupName</span></span>
<span data-ttu-id="fdb56-113">備份名稱</span><span class="sxs-lookup"><span data-stu-id="fdb56-113">Backup Name</span></span>

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

### <span data-ttu-id="fdb56-114">-資料庫</span><span class="sxs-lookup"><span data-stu-id="fdb56-114">-Databases</span></span>
<span data-ttu-id="fdb56-115">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="fdb56-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="fdb56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb56-116">-DefaultProfile</span></span>
<span data-ttu-id="fdb56-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdb56-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb56-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdb56-118">-Name</span></span>
<span data-ttu-id="fdb56-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="fdb56-119">WebApp Name</span></span>

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

### <span data-ttu-id="fdb56-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb56-120">-ResourceGroupName</span></span>
<span data-ttu-id="fdb56-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fdb56-121">Resource Group Name</span></span>

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

### <span data-ttu-id="fdb56-122">-槽</span><span class="sxs-lookup"><span data-stu-id="fdb56-122">-Slot</span></span>
<span data-ttu-id="fdb56-123">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="fdb56-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fdb56-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="fdb56-124">-StorageAccountUrl</span></span>
<span data-ttu-id="fdb56-125">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="fdb56-125">Storage Account Url</span></span>

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

### <span data-ttu-id="fdb56-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fdb56-126">-WebApp</span></span>
<span data-ttu-id="fdb56-127">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="fdb56-127">WebApp Object</span></span>

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

### <span data-ttu-id="fdb56-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb56-128">CommonParameters</span></span>
<span data-ttu-id="fdb56-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdb56-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb56-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdb56-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb56-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fdb56-131">INPUTS</span></span>

### <span data-ttu-id="fdb56-132">網站地圖</span><span class="sxs-lookup"><span data-stu-id="fdb56-132">Site</span></span>
<span data-ttu-id="fdb56-133">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fdb56-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fdb56-134">輸出</span><span class="sxs-lookup"><span data-stu-id="fdb56-134">OUTPUTS</span></span>

### <span data-ttu-id="fdb56-135">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="fdb56-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="fdb56-136">筆記</span><span class="sxs-lookup"><span data-stu-id="fdb56-136">NOTES</span></span>

## <span data-ttu-id="fdb56-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdb56-137">RELATED LINKS</span></span>

