---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: 7b3e721adaa0389f1c2a75750d7bf36dfe4c2ac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623397"
---
# <span data-ttu-id="90843-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="90843-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="90843-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90843-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90843-103">句法</span><span class="sxs-lookup"><span data-stu-id="90843-103">SYNTAX</span></span>

### <span data-ttu-id="90843-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="90843-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90843-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="90843-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90843-106">說明</span><span class="sxs-lookup"><span data-stu-id="90843-106">DESCRIPTION</span></span>
<span data-ttu-id="90843-107">**AzureRmWebAppBackup** Cmdlet 會取得 Azure Web App 的指定備份。</span><span class="sxs-lookup"><span data-stu-id="90843-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="90843-108">示例</span><span class="sxs-lookup"><span data-stu-id="90843-108">EXAMPLES</span></span>

### <span data-ttu-id="90843-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="90843-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="90843-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為「WebAppStandard」的 Web App 中，取得 ID 為「12345」的備份。</span><span class="sxs-lookup"><span data-stu-id="90843-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="90843-111">參數</span><span class="sxs-lookup"><span data-stu-id="90843-111">PARAMETERS</span></span>

### <span data-ttu-id="90843-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="90843-112">-BackupId</span></span>
<span data-ttu-id="90843-113">備份識別碼</span><span class="sxs-lookup"><span data-stu-id="90843-113">Backup Id</span></span>

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

### <span data-ttu-id="90843-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90843-114">-DefaultProfile</span></span>
<span data-ttu-id="90843-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90843-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90843-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="90843-116">-Name</span></span>
<span data-ttu-id="90843-117">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="90843-117">Webapp Name</span></span>

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

### <span data-ttu-id="90843-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90843-118">-ResourceGroupName</span></span>
<span data-ttu-id="90843-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="90843-119">Resource Group Name</span></span>

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

### <span data-ttu-id="90843-120">-槽</span><span class="sxs-lookup"><span data-stu-id="90843-120">-Slot</span></span>
<span data-ttu-id="90843-121">槽名稱</span><span class="sxs-lookup"><span data-stu-id="90843-121">Slot Name</span></span>

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

### <span data-ttu-id="90843-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="90843-122">-WebApp</span></span>
<span data-ttu-id="90843-123">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="90843-123">Piped WebApp</span></span>

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

### <span data-ttu-id="90843-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90843-124">CommonParameters</span></span>
<span data-ttu-id="90843-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90843-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90843-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90843-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90843-127">輸入</span><span class="sxs-lookup"><span data-stu-id="90843-127">INPUTS</span></span>

### <span data-ttu-id="90843-128">System.object</span><span class="sxs-lookup"><span data-stu-id="90843-128">System.String</span></span>

### <span data-ttu-id="90843-129">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="90843-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="90843-130">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="90843-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="90843-131">輸出</span><span class="sxs-lookup"><span data-stu-id="90843-131">OUTPUTS</span></span>

### <span data-ttu-id="90843-132">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="90843-132">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="90843-133">筆記</span><span class="sxs-lookup"><span data-stu-id="90843-133">NOTES</span></span>

## <span data-ttu-id="90843-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="90843-134">RELATED LINKS</span></span>
