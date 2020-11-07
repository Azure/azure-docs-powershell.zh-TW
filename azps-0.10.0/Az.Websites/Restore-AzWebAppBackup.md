---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: f93a173e79cb34c5603ce58fc3e03c92869a5d01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794944"
---
# <span data-ttu-id="45f84-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="45f84-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="45f84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45f84-102">SYNOPSIS</span></span>

## <span data-ttu-id="45f84-103">句法</span><span class="sxs-lookup"><span data-stu-id="45f84-103">SYNTAX</span></span>

### <span data-ttu-id="45f84-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="45f84-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="45f84-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="45f84-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="45f84-106">說明</span><span class="sxs-lookup"><span data-stu-id="45f84-106">DESCRIPTION</span></span>
<span data-ttu-id="45f84-107">**Restore-AzWebAppBackup** Cmdlet 會還原 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="45f84-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="45f84-108">示例</span><span class="sxs-lookup"><span data-stu-id="45f84-108">EXAMPLES</span></span>

### <span data-ttu-id="45f84-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="45f84-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="45f84-110">還原位於「myBlob」的 [資源群組] 中的指定 app ContosoWebApp 的備份（位於 [WestUS] blob ""） https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="45f84-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="45f84-111">參數</span><span class="sxs-lookup"><span data-stu-id="45f84-111">PARAMETERS</span></span>

### <span data-ttu-id="45f84-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="45f84-112">-AppServicePlan</span></span>
<span data-ttu-id="45f84-113">已還原之應用程式的應用程式服務方案名稱。</span><span class="sxs-lookup"><span data-stu-id="45f84-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="45f84-114">如果保留空白，則會使用 app 的目前 App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="45f84-114">If left empty, the app's current App Service Plan is used.</span></span>
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

### <span data-ttu-id="45f84-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="45f84-115">-BlobName</span></span>
<span data-ttu-id="45f84-116">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="45f84-116">Blob Name</span></span>

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

### <span data-ttu-id="45f84-117">-資料庫</span><span class="sxs-lookup"><span data-stu-id="45f84-117">-Databases</span></span>
<span data-ttu-id="45f84-118">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="45f84-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="45f84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f84-119">-DefaultProfile</span></span>
<span data-ttu-id="45f84-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45f84-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45f84-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="45f84-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="45f84-122">忽略衝突的主機名稱選項</span><span class="sxs-lookup"><span data-stu-id="45f84-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="45f84-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="45f84-123">-Name</span></span>
<span data-ttu-id="45f84-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="45f84-124">WebApp Name</span></span>

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

### <span data-ttu-id="45f84-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="45f84-125">-Overwrite</span></span>
<span data-ttu-id="45f84-126">覆寫選項</span><span class="sxs-lookup"><span data-stu-id="45f84-126">Overwrite Option</span></span>

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

### <span data-ttu-id="45f84-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45f84-127">-ResourceGroupName</span></span>
<span data-ttu-id="45f84-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="45f84-128">Resource Group Name</span></span>

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

### <span data-ttu-id="45f84-129">-槽</span><span class="sxs-lookup"><span data-stu-id="45f84-129">-Slot</span></span>
<span data-ttu-id="45f84-130">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="45f84-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="45f84-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="45f84-131">-StorageAccountUrl</span></span>
<span data-ttu-id="45f84-132">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="45f84-132">Storage Account Url</span></span>

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

### <span data-ttu-id="45f84-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="45f84-133">-WebApp</span></span>
<span data-ttu-id="45f84-134">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="45f84-134">WebApp Object</span></span>

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

### <span data-ttu-id="45f84-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f84-135">CommonParameters</span></span>
<span data-ttu-id="45f84-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45f84-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f84-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45f84-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f84-138">輸入</span><span class="sxs-lookup"><span data-stu-id="45f84-138">INPUTS</span></span>

### <span data-ttu-id="45f84-139">網站地圖</span><span class="sxs-lookup"><span data-stu-id="45f84-139">Site</span></span>
<span data-ttu-id="45f84-140">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="45f84-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="45f84-141">輸出</span><span class="sxs-lookup"><span data-stu-id="45f84-141">OUTPUTS</span></span>

## <span data-ttu-id="45f84-142">筆記</span><span class="sxs-lookup"><span data-stu-id="45f84-142">NOTES</span></span>

## <span data-ttu-id="45f84-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="45f84-143">RELATED LINKS</span></span>

