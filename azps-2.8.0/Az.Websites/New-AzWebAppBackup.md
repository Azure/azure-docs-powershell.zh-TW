---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 2ef015c3f793dd4636632f17568feb9aaf1b5ad2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793310"
---
# <span data-ttu-id="54b6a-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="54b6a-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="54b6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54b6a-102">SYNOPSIS</span></span>

## <span data-ttu-id="54b6a-103">句法</span><span class="sxs-lookup"><span data-stu-id="54b6a-103">SYNTAX</span></span>

### <span data-ttu-id="54b6a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="54b6a-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="54b6a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="54b6a-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="54b6a-106">說明</span><span class="sxs-lookup"><span data-stu-id="54b6a-106">DESCRIPTION</span></span>
<span data-ttu-id="54b6a-107">**新的-AzWebAppBackup** Cmdlet 會建立 Azure Web App 備份。</span><span class="sxs-lookup"><span data-stu-id="54b6a-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="54b6a-108">示例</span><span class="sxs-lookup"><span data-stu-id="54b6a-108">EXAMPLES</span></span>

### <span data-ttu-id="54b6a-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="54b6a-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="54b6a-110">在「資源群組預設-Web-WestUS」中建立指定 app ContosoWebApp 的備份 https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="54b6a-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="54b6a-111">參數</span><span class="sxs-lookup"><span data-stu-id="54b6a-111">PARAMETERS</span></span>

### <span data-ttu-id="54b6a-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="54b6a-112">-BackupName</span></span>
<span data-ttu-id="54b6a-113">備份名稱</span><span class="sxs-lookup"><span data-stu-id="54b6a-113">Backup Name</span></span>

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

### <span data-ttu-id="54b6a-114">-資料庫</span><span class="sxs-lookup"><span data-stu-id="54b6a-114">-Databases</span></span>
<span data-ttu-id="54b6a-115">類型 DatabaseBackupSetting [] 的資料庫</span><span class="sxs-lookup"><span data-stu-id="54b6a-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="54b6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b6a-116">-DefaultProfile</span></span>
<span data-ttu-id="54b6a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54b6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54b6a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="54b6a-118">-Name</span></span>
<span data-ttu-id="54b6a-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="54b6a-119">WebApp Name</span></span>

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

### <span data-ttu-id="54b6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="54b6a-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="54b6a-121">Resource Group Name</span></span>

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

### <span data-ttu-id="54b6a-122">-槽</span><span class="sxs-lookup"><span data-stu-id="54b6a-122">-Slot</span></span>
<span data-ttu-id="54b6a-123">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="54b6a-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="54b6a-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="54b6a-124">-StorageAccountUrl</span></span>
<span data-ttu-id="54b6a-125">儲存空間帳戶 Url</span><span class="sxs-lookup"><span data-stu-id="54b6a-125">Storage Account Url</span></span>

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

### <span data-ttu-id="54b6a-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="54b6a-126">-WebApp</span></span>
<span data-ttu-id="54b6a-127">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="54b6a-127">WebApp Object</span></span>

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

### <span data-ttu-id="54b6a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b6a-128">CommonParameters</span></span>
<span data-ttu-id="54b6a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54b6a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b6a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54b6a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b6a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="54b6a-131">INPUTS</span></span>

### <span data-ttu-id="54b6a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="54b6a-132">System.String</span></span>

### <span data-ttu-id="54b6a-133">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="54b6a-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="54b6a-134">DatabaseBackupSetting [] 的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="54b6a-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="54b6a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="54b6a-135">OUTPUTS</span></span>

### <span data-ttu-id="54b6a-136">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="54b6a-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="54b6a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="54b6a-137">NOTES</span></span>

## <span data-ttu-id="54b6a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="54b6a-138">RELATED LINKS</span></span>
