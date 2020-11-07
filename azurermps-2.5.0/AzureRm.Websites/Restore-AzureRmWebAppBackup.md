---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801854"
---
# <span data-ttu-id="bd2fc-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="bd2fc-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="bd2fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd2fc-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd2fc-103">句法</span><span class="sxs-lookup"><span data-stu-id="bd2fc-103">SYNTAX</span></span>

### <span data-ttu-id="bd2fc-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="bd2fc-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="bd2fc-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="bd2fc-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="bd2fc-106">說明</span><span class="sxs-lookup"><span data-stu-id="bd2fc-106">DESCRIPTION</span></span>
<span data-ttu-id="bd2fc-107">**Restore-AzureRmWebAppBackup** Cmdlet 會還原 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="bd2fc-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="bd2fc-108">示例</span><span class="sxs-lookup"><span data-stu-id="bd2fc-108">EXAMPLES</span></span>

### <span data-ttu-id="bd2fc-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="bd2fc-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="bd2fc-110">還原位於「myBlob」的 [資源群組] 中的指定 app ContosoWebApp 的備份（位於 [WestUS] blob ""） https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="bd2fc-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="bd2fc-111">參數</span><span class="sxs-lookup"><span data-stu-id="bd2fc-111">PARAMETERS</span></span>

### <span data-ttu-id="bd2fc-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bd2fc-112">-AppServicePlan</span></span>
<span data-ttu-id="bd2fc-113">已還原之應用程式的應用程式服務方案名稱。</span><span class="sxs-lookup"><span data-stu-id="bd2fc-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="bd2fc-114">如果保留空白，則會使用 app 的目前 App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="bd2fc-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2fc-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="bd2fc-115">-BlobName</span></span>
<span data-ttu-id="bd2fc-116">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="bd2fc-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2fc-117">-資料庫</span><span class="sxs-lookup"><span data-stu-id="bd2fc-117">-Databases</span></span>
<span data-ttu-id="bd2fc-118">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="bd2fc-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="bd2fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2fc-119">-DefaultProfile</span></span>
<span data-ttu-id="bd2fc-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd2fc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd2fc-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="bd2fc-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="bd2fc-122">忽略衝突的主機名稱選項</span><span class="sxs-lookup"><span data-stu-id="bd2fc-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2fc-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd2fc-123">-Name</span></span>
<span data-ttu-id="bd2fc-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="bd2fc-124">WebApp Name</span></span>

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

### <span data-ttu-id="bd2fc-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="bd2fc-125">-Overwrite</span></span>
<span data-ttu-id="bd2fc-126">覆寫選項</span><span class="sxs-lookup"><span data-stu-id="bd2fc-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd2fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd2fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd2fc-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bd2fc-128">Resource Group Name</span></span>

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

### <span data-ttu-id="bd2fc-129">-槽</span><span class="sxs-lookup"><span data-stu-id="bd2fc-129">-Slot</span></span>
<span data-ttu-id="bd2fc-130">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="bd2fc-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bd2fc-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="bd2fc-131">-StorageAccountUrl</span></span>
<span data-ttu-id="bd2fc-132">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="bd2fc-132">Storage Account Url</span></span>

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

### <span data-ttu-id="bd2fc-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bd2fc-133">-WebApp</span></span>
<span data-ttu-id="bd2fc-134">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="bd2fc-134">WebApp Object</span></span>

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

### <span data-ttu-id="bd2fc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2fc-135">CommonParameters</span></span>
<span data-ttu-id="bd2fc-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd2fc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2fc-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd2fc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2fc-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bd2fc-138">INPUTS</span></span>

### <span data-ttu-id="bd2fc-139">網站地圖</span><span class="sxs-lookup"><span data-stu-id="bd2fc-139">Site</span></span>
<span data-ttu-id="bd2fc-140">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="bd2fc-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bd2fc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bd2fc-141">OUTPUTS</span></span>

## <span data-ttu-id="bd2fc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="bd2fc-142">NOTES</span></span>

## <span data-ttu-id="bd2fc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd2fc-143">RELATED LINKS</span></span>

