---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: c6d5809211910987e06cff024d7510a70ad71a4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799709"
---
# <span data-ttu-id="206ca-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="206ca-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="206ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="206ca-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="206ca-103">句法</span><span class="sxs-lookup"><span data-stu-id="206ca-103">SYNTAX</span></span>

### <span data-ttu-id="206ca-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="206ca-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="206ca-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="206ca-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="206ca-106">說明</span><span class="sxs-lookup"><span data-stu-id="206ca-106">DESCRIPTION</span></span>
<span data-ttu-id="206ca-107">**AzureRmWebAppBackup** Cmdlet 會取得 Azure Web App 的指定備份。</span><span class="sxs-lookup"><span data-stu-id="206ca-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="206ca-108">示例</span><span class="sxs-lookup"><span data-stu-id="206ca-108">EXAMPLES</span></span>

### <span data-ttu-id="206ca-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="206ca-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="206ca-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為「WebAppStandard」的 Web App 中，取得 ID 為「12345」的備份。</span><span class="sxs-lookup"><span data-stu-id="206ca-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="206ca-111">參數</span><span class="sxs-lookup"><span data-stu-id="206ca-111">PARAMETERS</span></span>

### <span data-ttu-id="206ca-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="206ca-112">-BackupId</span></span>
<span data-ttu-id="206ca-113">備份識別碼</span><span class="sxs-lookup"><span data-stu-id="206ca-113">Backup Id</span></span>

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

### <span data-ttu-id="206ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206ca-114">-DefaultProfile</span></span>
<span data-ttu-id="206ca-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="206ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="206ca-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="206ca-116">-Name</span></span>
<span data-ttu-id="206ca-117">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="206ca-117">Webapp Name</span></span>

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

### <span data-ttu-id="206ca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206ca-118">-ResourceGroupName</span></span>
<span data-ttu-id="206ca-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="206ca-119">Resource Group Name</span></span>

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

### <span data-ttu-id="206ca-120">-槽</span><span class="sxs-lookup"><span data-stu-id="206ca-120">-Slot</span></span>
<span data-ttu-id="206ca-121">槽名稱</span><span class="sxs-lookup"><span data-stu-id="206ca-121">Slot Name</span></span>

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

### <span data-ttu-id="206ca-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="206ca-122">-WebApp</span></span>
<span data-ttu-id="206ca-123">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="206ca-123">Piped WebApp</span></span>

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

### <span data-ttu-id="206ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206ca-124">CommonParameters</span></span>
<span data-ttu-id="206ca-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="206ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206ca-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="206ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206ca-127">輸入</span><span class="sxs-lookup"><span data-stu-id="206ca-127">INPUTS</span></span>

### <span data-ttu-id="206ca-128">網站地圖</span><span class="sxs-lookup"><span data-stu-id="206ca-128">Site</span></span>
<span data-ttu-id="206ca-129">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="206ca-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="206ca-130">輸出</span><span class="sxs-lookup"><span data-stu-id="206ca-130">OUTPUTS</span></span>

### <span data-ttu-id="206ca-131">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="206ca-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="206ca-132">筆記</span><span class="sxs-lookup"><span data-stu-id="206ca-132">NOTES</span></span>

## <span data-ttu-id="206ca-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="206ca-133">RELATED LINKS</span></span>

