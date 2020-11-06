---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447897"
---
# <span data-ttu-id="1946c-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1946c-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1946c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1946c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1946c-103">句法</span><span class="sxs-lookup"><span data-stu-id="1946c-103">SYNTAX</span></span>

### <span data-ttu-id="1946c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1946c-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="1946c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1946c-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="1946c-106">說明</span><span class="sxs-lookup"><span data-stu-id="1946c-106">DESCRIPTION</span></span>
<span data-ttu-id="1946c-107">**AzureRmWebAppBackupConfiguration** Cmdlet 編輯 Azure Web App 目前的配置備份。</span><span class="sxs-lookup"><span data-stu-id="1946c-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="1946c-108">示例</span><span class="sxs-lookup"><span data-stu-id="1946c-108">EXAMPLES</span></span>

## <span data-ttu-id="1946c-109">參數</span><span class="sxs-lookup"><span data-stu-id="1946c-109">PARAMETERS</span></span>

### <span data-ttu-id="1946c-110">-資料庫</span><span class="sxs-lookup"><span data-stu-id="1946c-110">-Databases</span></span>
<span data-ttu-id="1946c-111">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="1946c-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1946c-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="1946c-112">-FrequencyInterval</span></span>
<span data-ttu-id="1946c-113">頻率間隔</span><span class="sxs-lookup"><span data-stu-id="1946c-113">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1946c-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="1946c-114">-FrequencyUnit</span></span>
<span data-ttu-id="1946c-115">Frequency 單位</span><span class="sxs-lookup"><span data-stu-id="1946c-115">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1946c-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="1946c-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="1946c-117">保留至少一個備份選項</span><span class="sxs-lookup"><span data-stu-id="1946c-117">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1946c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1946c-118">-Name</span></span>
<span data-ttu-id="1946c-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="1946c-119">WebApp Name</span></span>

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

### <span data-ttu-id="1946c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1946c-120">-ResourceGroupName</span></span>
<span data-ttu-id="1946c-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1946c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="1946c-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1946c-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="1946c-123">保留期間（天）</span><span class="sxs-lookup"><span data-stu-id="1946c-123">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1946c-124">-槽</span><span class="sxs-lookup"><span data-stu-id="1946c-124">-Slot</span></span>
<span data-ttu-id="1946c-125">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="1946c-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1946c-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1946c-126">-StartTime</span></span>
<span data-ttu-id="1946c-127">UTC 中的 StartTime</span><span class="sxs-lookup"><span data-stu-id="1946c-127">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1946c-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="1946c-128">-StorageAccountUrl</span></span>
<span data-ttu-id="1946c-129">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="1946c-129">Storage Account Url</span></span>

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

### <span data-ttu-id="1946c-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1946c-130">-WebApp</span></span>
<span data-ttu-id="1946c-131">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="1946c-131">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1946c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1946c-132">-DefaultProfile</span></span>
<span data-ttu-id="1946c-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1946c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1946c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1946c-134">CommonParameters</span></span>
<span data-ttu-id="1946c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1946c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1946c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1946c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1946c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1946c-137">INPUTS</span></span>

### <span data-ttu-id="1946c-138">網站地圖</span><span class="sxs-lookup"><span data-stu-id="1946c-138">Site</span></span>
<span data-ttu-id="1946c-139">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1946c-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1946c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1946c-140">OUTPUTS</span></span>

### <span data-ttu-id="1946c-141">WebApps WebApps. AzureWebAppBackupConfiguration （）</span><span class="sxs-lookup"><span data-stu-id="1946c-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1946c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1946c-142">NOTES</span></span>

## <span data-ttu-id="1946c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1946c-143">RELATED LINKS</span></span>

[<span data-ttu-id="1946c-144">AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1946c-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


