---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 3ff0d45abfbe00da2e56bc915d1264efe5f387ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129067"
---
# <span data-ttu-id="5adef-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5adef-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="5adef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5adef-102">SYNOPSIS</span></span>

## <span data-ttu-id="5adef-103">句法</span><span class="sxs-lookup"><span data-stu-id="5adef-103">SYNTAX</span></span>

### <span data-ttu-id="5adef-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5adef-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="5adef-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5adef-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="5adef-106">說明</span><span class="sxs-lookup"><span data-stu-id="5adef-106">DESCRIPTION</span></span>
<span data-ttu-id="5adef-107">**新的-AzWebAppBackup** Cmdlet 會建立 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="5adef-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="5adef-108">示例</span><span class="sxs-lookup"><span data-stu-id="5adef-108">EXAMPLES</span></span>

### <span data-ttu-id="5adef-109">範例1</span><span class="sxs-lookup"><span data-stu-id="5adef-109">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="5adef-110">在「資源群組預設-Web-WestUS」中建立指定 app ContosoWebApp 的備份 https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="5adef-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

### <span data-ttu-id="5adef-111">範例2</span><span class="sxs-lookup"><span data-stu-id="5adef-111">Example 2</span></span>

<span data-ttu-id="5adef-112">New-AzWebAppBackup Cmdlet 會建立 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="5adef-112">The New-AzWebAppBackup cmdlet creates an Azure Web App Backup.</span></span> <span data-ttu-id="5adef-113"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="5adef-113">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppBackup -BackupName <String> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -StorageAccountUrl 'https://storageaccount.file.core.windows.net'
```

## <span data-ttu-id="5adef-114">參數</span><span class="sxs-lookup"><span data-stu-id="5adef-114">PARAMETERS</span></span>

### <span data-ttu-id="5adef-115">-BackupName</span><span class="sxs-lookup"><span data-stu-id="5adef-115">-BackupName</span></span>
<span data-ttu-id="5adef-116">備份名稱</span><span class="sxs-lookup"><span data-stu-id="5adef-116">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5adef-117">-資料庫</span><span class="sxs-lookup"><span data-stu-id="5adef-117">-Databases</span></span>
<span data-ttu-id="5adef-118">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="5adef-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="5adef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5adef-119">-DefaultProfile</span></span>
<span data-ttu-id="5adef-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5adef-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5adef-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5adef-121">-Name</span></span>
<span data-ttu-id="5adef-122">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="5adef-122">WebApp Name</span></span>

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

### <span data-ttu-id="5adef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5adef-123">-ResourceGroupName</span></span>
<span data-ttu-id="5adef-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5adef-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5adef-125">-槽</span><span class="sxs-lookup"><span data-stu-id="5adef-125">-Slot</span></span>
<span data-ttu-id="5adef-126">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="5adef-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5adef-127">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="5adef-127">-StorageAccountUrl</span></span>
<span data-ttu-id="5adef-128">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="5adef-128">Storage Account Url</span></span>

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

### <span data-ttu-id="5adef-129">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5adef-129">-WebApp</span></span>
<span data-ttu-id="5adef-130">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="5adef-130">WebApp Object</span></span>

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

### <span data-ttu-id="5adef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5adef-131">CommonParameters</span></span>
<span data-ttu-id="5adef-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5adef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5adef-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5adef-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5adef-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5adef-134">INPUTS</span></span>

### <span data-ttu-id="5adef-135">System.object</span><span class="sxs-lookup"><span data-stu-id="5adef-135">System.String</span></span>

### <span data-ttu-id="5adef-136">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="5adef-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="5adef-137">DatabaseBackupSetting [] 的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="5adef-137">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="5adef-138">輸出</span><span class="sxs-lookup"><span data-stu-id="5adef-138">OUTPUTS</span></span>

### <span data-ttu-id="5adef-139">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="5adef-139">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="5adef-140">筆記</span><span class="sxs-lookup"><span data-stu-id="5adef-140">NOTES</span></span>

## <span data-ttu-id="5adef-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5adef-141">RELATED LINKS</span></span>