---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624518"
---
# <span data-ttu-id="96c71-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="96c71-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="96c71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96c71-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96c71-103">句法</span><span class="sxs-lookup"><span data-stu-id="96c71-103">SYNTAX</span></span>

### <span data-ttu-id="96c71-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="96c71-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c71-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="96c71-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96c71-106">說明</span><span class="sxs-lookup"><span data-stu-id="96c71-106">DESCRIPTION</span></span>
<span data-ttu-id="96c71-107">**AzureRmWebAppBackupConfiguration** Cmdlet 會取得 Azure Web App 的備份設定。</span><span class="sxs-lookup"><span data-stu-id="96c71-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="96c71-108">示例</span><span class="sxs-lookup"><span data-stu-id="96c71-108">EXAMPLES</span></span>

### <span data-ttu-id="96c71-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="96c71-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="96c71-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為 WebAppStandard 的 Web App 取得備份配置。</span><span class="sxs-lookup"><span data-stu-id="96c71-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="96c71-111">參數</span><span class="sxs-lookup"><span data-stu-id="96c71-111">PARAMETERS</span></span>

### <span data-ttu-id="96c71-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="96c71-112">-Name</span></span>
<span data-ttu-id="96c71-113">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="96c71-113">WebApp Name</span></span>

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

### <span data-ttu-id="96c71-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c71-114">-ResourceGroupName</span></span>
<span data-ttu-id="96c71-115">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="96c71-115">Resource Group Name</span></span>

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

### <span data-ttu-id="96c71-116">-槽</span><span class="sxs-lookup"><span data-stu-id="96c71-116">-Slot</span></span>
<span data-ttu-id="96c71-117">槽名稱</span><span class="sxs-lookup"><span data-stu-id="96c71-117">Slot Name</span></span>

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

### <span data-ttu-id="96c71-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="96c71-118">-WebApp</span></span>
<span data-ttu-id="96c71-119">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="96c71-119">WebApp Name</span></span>

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

### <span data-ttu-id="96c71-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c71-120">-DefaultProfile</span></span>
<span data-ttu-id="96c71-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96c71-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c71-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c71-122">CommonParameters</span></span>
<span data-ttu-id="96c71-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96c71-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c71-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96c71-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c71-125">輸入</span><span class="sxs-lookup"><span data-stu-id="96c71-125">INPUTS</span></span>

### <span data-ttu-id="96c71-126">網站地圖</span><span class="sxs-lookup"><span data-stu-id="96c71-126">Site</span></span>
<span data-ttu-id="96c71-127">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="96c71-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="96c71-128">輸出</span><span class="sxs-lookup"><span data-stu-id="96c71-128">OUTPUTS</span></span>

### <span data-ttu-id="96c71-129">WebApps WebApps. AzureWebAppBackupConfiguration （）</span><span class="sxs-lookup"><span data-stu-id="96c71-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="96c71-130">筆記</span><span class="sxs-lookup"><span data-stu-id="96c71-130">NOTES</span></span>

## <span data-ttu-id="96c71-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="96c71-131">RELATED LINKS</span></span>

