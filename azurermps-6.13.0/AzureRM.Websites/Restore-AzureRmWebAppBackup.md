---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: efb570c22b5345b9d75fdf96dca061dc5cf7847f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449654"
---
# <span data-ttu-id="4781b-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="4781b-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="4781b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4781b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4781b-103">句法</span><span class="sxs-lookup"><span data-stu-id="4781b-103">SYNTAX</span></span>

### <span data-ttu-id="4781b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4781b-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="4781b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4781b-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="4781b-106">說明</span><span class="sxs-lookup"><span data-stu-id="4781b-106">DESCRIPTION</span></span>
<span data-ttu-id="4781b-107">**Restore-AzureRmWebAppBackup** Cmdlet 會還原 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="4781b-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="4781b-108">示例</span><span class="sxs-lookup"><span data-stu-id="4781b-108">EXAMPLES</span></span>

### <span data-ttu-id="4781b-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="4781b-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="4781b-110">還原位於「myBlob」的 [資源群組] 中的指定 app ContosoWebApp 的備份（位於 [WestUS] blob ""） https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="4781b-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="4781b-111">參數</span><span class="sxs-lookup"><span data-stu-id="4781b-111">PARAMETERS</span></span>

### <span data-ttu-id="4781b-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4781b-112">-AppServicePlan</span></span>
<span data-ttu-id="4781b-113">已還原之應用程式的應用程式服務方案名稱。</span><span class="sxs-lookup"><span data-stu-id="4781b-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="4781b-114">如果保留空白，則會使用 app 的目前 App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="4781b-114">If left empty, the app's current App Service Plan is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="4781b-115">-BlobName</span></span>
<span data-ttu-id="4781b-116">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="4781b-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-117">-資料庫</span><span class="sxs-lookup"><span data-stu-id="4781b-117">-Databases</span></span>
<span data-ttu-id="4781b-118">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="4781b-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4781b-119">-DefaultProfile</span></span>
<span data-ttu-id="4781b-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4781b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4781b-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="4781b-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="4781b-122">忽略衝突的主機名稱選項</span><span class="sxs-lookup"><span data-stu-id="4781b-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4781b-123">-Name</span></span>
<span data-ttu-id="4781b-124">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="4781b-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4781b-125">-Overwrite</span></span>
<span data-ttu-id="4781b-126">覆寫選項</span><span class="sxs-lookup"><span data-stu-id="4781b-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4781b-127">-ResourceGroupName</span></span>
<span data-ttu-id="4781b-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4781b-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-129">-槽</span><span class="sxs-lookup"><span data-stu-id="4781b-129">-Slot</span></span>
<span data-ttu-id="4781b-130">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="4781b-130">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="4781b-131">-StorageAccountUrl</span></span>
<span data-ttu-id="4781b-132">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="4781b-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4781b-133">-WebApp</span></span>
<span data-ttu-id="4781b-134">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="4781b-134">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4781b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4781b-135">CommonParameters</span></span>
<span data-ttu-id="4781b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4781b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4781b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4781b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4781b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4781b-138">INPUTS</span></span>

### <span data-ttu-id="4781b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="4781b-139">System.String</span></span>

### <span data-ttu-id="4781b-140">DatabaseBackupSetting [] 的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="4781b-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="4781b-141">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4781b-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4781b-142">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="4781b-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="4781b-143">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4781b-143">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="4781b-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4781b-144">OUTPUTS</span></span>

### <span data-ttu-id="4781b-145">System.void</span><span class="sxs-lookup"><span data-stu-id="4781b-145">System.Void</span></span>

## <span data-ttu-id="4781b-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4781b-146">NOTES</span></span>

## <span data-ttu-id="4781b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="4781b-147">RELATED LINKS</span></span>
