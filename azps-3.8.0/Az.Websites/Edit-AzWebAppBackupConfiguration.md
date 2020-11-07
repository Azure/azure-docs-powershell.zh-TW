---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 490f7b4a0cb723d02deb1d18e8a2ddfb993e7f0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957619"
---
# <span data-ttu-id="2bbfd-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bbfd-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="2bbfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bbfd-102">SYNOPSIS</span></span>

## <span data-ttu-id="2bbfd-103">句法</span><span class="sxs-lookup"><span data-stu-id="2bbfd-103">SYNTAX</span></span>

### <span data-ttu-id="2bbfd-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2bbfd-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="2bbfd-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2bbfd-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="2bbfd-106">說明</span><span class="sxs-lookup"><span data-stu-id="2bbfd-106">DESCRIPTION</span></span>
<span data-ttu-id="2bbfd-107">**AzWebAppBackupConfiguration** Cmdlet 編輯 Azure Web App 目前的配置備份。</span><span class="sxs-lookup"><span data-stu-id="2bbfd-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="2bbfd-108">示例</span><span class="sxs-lookup"><span data-stu-id="2bbfd-108">EXAMPLES</span></span>

## <span data-ttu-id="2bbfd-109">參數</span><span class="sxs-lookup"><span data-stu-id="2bbfd-109">PARAMETERS</span></span>

### <span data-ttu-id="2bbfd-110">-資料庫</span><span class="sxs-lookup"><span data-stu-id="2bbfd-110">-Databases</span></span>
<span data-ttu-id="2bbfd-111">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="2bbfd-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="2bbfd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbfd-112">-DefaultProfile</span></span>
<span data-ttu-id="2bbfd-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bbfd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bbfd-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="2bbfd-114">-FrequencyInterval</span></span>
<span data-ttu-id="2bbfd-115">頻率間隔</span><span class="sxs-lookup"><span data-stu-id="2bbfd-115">Frequency Interval</span></span>

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

### <span data-ttu-id="2bbfd-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="2bbfd-116">-FrequencyUnit</span></span>
<span data-ttu-id="2bbfd-117">Frequency 單位</span><span class="sxs-lookup"><span data-stu-id="2bbfd-117">Frequency Unit</span></span>

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

### <span data-ttu-id="2bbfd-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="2bbfd-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="2bbfd-119">保留至少一個備份選項</span><span class="sxs-lookup"><span data-stu-id="2bbfd-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="2bbfd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bbfd-120">-Name</span></span>
<span data-ttu-id="2bbfd-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2bbfd-121">WebApp Name</span></span>

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

### <span data-ttu-id="2bbfd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bbfd-122">-ResourceGroupName</span></span>
<span data-ttu-id="2bbfd-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2bbfd-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2bbfd-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="2bbfd-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="2bbfd-125">保留期間（天）</span><span class="sxs-lookup"><span data-stu-id="2bbfd-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="2bbfd-126">-槽</span><span class="sxs-lookup"><span data-stu-id="2bbfd-126">-Slot</span></span>
<span data-ttu-id="2bbfd-127">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="2bbfd-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2bbfd-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2bbfd-128">-StartTime</span></span>
<span data-ttu-id="2bbfd-129">UTC 中的 StartTime</span><span class="sxs-lookup"><span data-stu-id="2bbfd-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="2bbfd-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="2bbfd-130">-StorageAccountUrl</span></span>
<span data-ttu-id="2bbfd-131">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="2bbfd-131">Storage Account Url</span></span>

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

### <span data-ttu-id="2bbfd-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2bbfd-132">-WebApp</span></span>
<span data-ttu-id="2bbfd-133">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2bbfd-133">WebApp Object</span></span>

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

### <span data-ttu-id="2bbfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbfd-134">CommonParameters</span></span>
<span data-ttu-id="2bbfd-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bbfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbfd-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bbfd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbfd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2bbfd-137">INPUTS</span></span>

### <span data-ttu-id="2bbfd-138">System.object</span><span class="sxs-lookup"><span data-stu-id="2bbfd-138">System.Int32</span></span>

### <span data-ttu-id="2bbfd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="2bbfd-139">System.String</span></span>

### <span data-ttu-id="2bbfd-140">System.object</span><span class="sxs-lookup"><span data-stu-id="2bbfd-140">System.DateTime</span></span>

### <span data-ttu-id="2bbfd-141">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2bbfd-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2bbfd-142">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="2bbfd-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="2bbfd-143">DatabaseBackupSetting [] 的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="2bbfd-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="2bbfd-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2bbfd-144">OUTPUTS</span></span>

### <span data-ttu-id="2bbfd-145">WebApps WebApps. AzureWebAppBackupConfiguration （）</span><span class="sxs-lookup"><span data-stu-id="2bbfd-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="2bbfd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2bbfd-146">NOTES</span></span>

## <span data-ttu-id="2bbfd-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bbfd-147">RELATED LINKS</span></span>

[<span data-ttu-id="2bbfd-148">AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bbfd-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


