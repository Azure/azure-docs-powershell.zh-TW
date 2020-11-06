---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452936"
---
# <span data-ttu-id="84bf9-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="84bf9-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="84bf9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84bf9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84bf9-103">句法</span><span class="sxs-lookup"><span data-stu-id="84bf9-103">SYNTAX</span></span>

### <span data-ttu-id="84bf9-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="84bf9-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="84bf9-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="84bf9-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="84bf9-106">說明</span><span class="sxs-lookup"><span data-stu-id="84bf9-106">DESCRIPTION</span></span>
<span data-ttu-id="84bf9-107">**Restore-AzureRmWebAppBackup** Cmdlet 會還原 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="84bf9-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="84bf9-108">示例</span><span class="sxs-lookup"><span data-stu-id="84bf9-108">EXAMPLES</span></span>

### <span data-ttu-id="84bf9-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="84bf9-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="84bf9-110">還原位於「myBlob」的 [資源群組] 中的指定 app ContosoWebApp 的備份（位於 [WestUS] blob ""） https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="84bf9-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="84bf9-111">參數</span><span class="sxs-lookup"><span data-stu-id="84bf9-111">PARAMETERS</span></span>

### <span data-ttu-id="84bf9-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="84bf9-112">-BlobName</span></span>
<span data-ttu-id="84bf9-113">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="84bf9-113">Blob Name</span></span>

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

### <span data-ttu-id="84bf9-114">-資料庫</span><span class="sxs-lookup"><span data-stu-id="84bf9-114">-Databases</span></span>
<span data-ttu-id="84bf9-115">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="84bf9-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="84bf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bf9-116">-DefaultProfile</span></span>
<span data-ttu-id="84bf9-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84bf9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84bf9-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="84bf9-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="84bf9-119">忽略衝突的主機名稱選項</span><span class="sxs-lookup"><span data-stu-id="84bf9-119">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="84bf9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="84bf9-120">-Name</span></span>
<span data-ttu-id="84bf9-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="84bf9-121">WebApp Name</span></span>

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

### <span data-ttu-id="84bf9-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="84bf9-122">-Overwrite</span></span>
<span data-ttu-id="84bf9-123">覆寫選項</span><span class="sxs-lookup"><span data-stu-id="84bf9-123">Overwrite Option</span></span>

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

### <span data-ttu-id="84bf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="84bf9-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="84bf9-125">Resource Group Name</span></span>

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

### <span data-ttu-id="84bf9-126">-槽</span><span class="sxs-lookup"><span data-stu-id="84bf9-126">-Slot</span></span>
<span data-ttu-id="84bf9-127">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="84bf9-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="84bf9-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="84bf9-128">-StorageAccountUrl</span></span>
<span data-ttu-id="84bf9-129">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="84bf9-129">Storage Account Url</span></span>

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

### <span data-ttu-id="84bf9-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="84bf9-130">-WebApp</span></span>
<span data-ttu-id="84bf9-131">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="84bf9-131">WebApp Object</span></span>

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

### <span data-ttu-id="84bf9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bf9-132">CommonParameters</span></span>
<span data-ttu-id="84bf9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84bf9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bf9-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84bf9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bf9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="84bf9-135">INPUTS</span></span>

### <span data-ttu-id="84bf9-136">網站地圖</span><span class="sxs-lookup"><span data-stu-id="84bf9-136">Site</span></span>
<span data-ttu-id="84bf9-137">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="84bf9-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="84bf9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="84bf9-138">OUTPUTS</span></span>

## <span data-ttu-id="84bf9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="84bf9-139">NOTES</span></span>

## <span data-ttu-id="84bf9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="84bf9-140">RELATED LINKS</span></span>
