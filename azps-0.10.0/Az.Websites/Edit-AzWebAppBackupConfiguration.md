---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795012"
---
# <span data-ttu-id="b839d-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b839d-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="b839d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b839d-102">SYNOPSIS</span></span>

## <span data-ttu-id="b839d-103">句法</span><span class="sxs-lookup"><span data-stu-id="b839d-103">SYNTAX</span></span>

### <span data-ttu-id="b839d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b839d-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="b839d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b839d-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="b839d-106">說明</span><span class="sxs-lookup"><span data-stu-id="b839d-106">DESCRIPTION</span></span>
<span data-ttu-id="b839d-107">**AzWebAppBackupConfiguration** Cmdlet 編輯 Azure Web App 目前的配置備份。</span><span class="sxs-lookup"><span data-stu-id="b839d-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="b839d-108">示例</span><span class="sxs-lookup"><span data-stu-id="b839d-108">EXAMPLES</span></span>

## <span data-ttu-id="b839d-109">參數</span><span class="sxs-lookup"><span data-stu-id="b839d-109">PARAMETERS</span></span>

### <span data-ttu-id="b839d-110">-資料庫</span><span class="sxs-lookup"><span data-stu-id="b839d-110">-Databases</span></span>
<span data-ttu-id="b839d-111">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="b839d-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b839d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b839d-112">-DefaultProfile</span></span>
<span data-ttu-id="b839d-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b839d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b839d-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="b839d-114">-FrequencyInterval</span></span>
<span data-ttu-id="b839d-115">頻率間隔</span><span class="sxs-lookup"><span data-stu-id="b839d-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b839d-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="b839d-116">-FrequencyUnit</span></span>
<span data-ttu-id="b839d-117">Frequency 單位</span><span class="sxs-lookup"><span data-stu-id="b839d-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b839d-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="b839d-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="b839d-119">保留至少一個備份選項</span><span class="sxs-lookup"><span data-stu-id="b839d-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b839d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b839d-120">-Name</span></span>
<span data-ttu-id="b839d-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="b839d-121">WebApp Name</span></span>

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

### <span data-ttu-id="b839d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b839d-122">-ResourceGroupName</span></span>
<span data-ttu-id="b839d-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b839d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b839d-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="b839d-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="b839d-125">保留期間（天）</span><span class="sxs-lookup"><span data-stu-id="b839d-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b839d-126">-槽</span><span class="sxs-lookup"><span data-stu-id="b839d-126">-Slot</span></span>
<span data-ttu-id="b839d-127">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="b839d-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b839d-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b839d-128">-StartTime</span></span>
<span data-ttu-id="b839d-129">UTC 中的 StartTime</span><span class="sxs-lookup"><span data-stu-id="b839d-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b839d-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b839d-130">-StorageAccountUrl</span></span>
<span data-ttu-id="b839d-131">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="b839d-131">Storage Account Url</span></span>

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

### <span data-ttu-id="b839d-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b839d-132">-WebApp</span></span>
<span data-ttu-id="b839d-133">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="b839d-133">WebApp Object</span></span>

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

### <span data-ttu-id="b839d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b839d-134">CommonParameters</span></span>
<span data-ttu-id="b839d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b839d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b839d-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b839d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b839d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b839d-137">INPUTS</span></span>

### <span data-ttu-id="b839d-138">網站地圖</span><span class="sxs-lookup"><span data-stu-id="b839d-138">Site</span></span>
<span data-ttu-id="b839d-139">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b839d-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b839d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b839d-140">OUTPUTS</span></span>

### <span data-ttu-id="b839d-141">WebApps WebApps. AzureWebAppBackupConfiguration （）</span><span class="sxs-lookup"><span data-stu-id="b839d-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="b839d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b839d-142">NOTES</span></span>

## <span data-ttu-id="b839d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b839d-143">RELATED LINKS</span></span>

[<span data-ttu-id="b839d-144">AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b839d-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


