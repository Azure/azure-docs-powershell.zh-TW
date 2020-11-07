---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 67bf9eb23318e4771c00760d18a5659526c5f45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800270"
---
# <span data-ttu-id="f4d6d-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4d6d-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f4d6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4d6d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4d6d-103">句法</span><span class="sxs-lookup"><span data-stu-id="f4d6d-103">SYNTAX</span></span>

### <span data-ttu-id="f4d6d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f4d6d-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4d6d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f4d6d-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4d6d-106">說明</span><span class="sxs-lookup"><span data-stu-id="f4d6d-106">DESCRIPTION</span></span>
<span data-ttu-id="f4d6d-107">**AzureRmWebAppBackupConfiguration** Cmdlet 會取得 Azure Web App 的備份設定。</span><span class="sxs-lookup"><span data-stu-id="f4d6d-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="f4d6d-108">示例</span><span class="sxs-lookup"><span data-stu-id="f4d6d-108">EXAMPLES</span></span>

### <span data-ttu-id="f4d6d-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="f4d6d-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="f4d6d-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為 WebAppStandard 的 Web App 取得備份配置。</span><span class="sxs-lookup"><span data-stu-id="f4d6d-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f4d6d-111">參數</span><span class="sxs-lookup"><span data-stu-id="f4d6d-111">PARAMETERS</span></span>

### <span data-ttu-id="f4d6d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d6d-112">-DefaultProfile</span></span>
<span data-ttu-id="f4d6d-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4d6d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4d6d-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4d6d-114">-Name</span></span>
<span data-ttu-id="f4d6d-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="f4d6d-115">WebApp Name</span></span>

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

### <span data-ttu-id="f4d6d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d6d-116">-ResourceGroupName</span></span>
<span data-ttu-id="f4d6d-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f4d6d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f4d6d-118">-槽</span><span class="sxs-lookup"><span data-stu-id="f4d6d-118">-Slot</span></span>
<span data-ttu-id="f4d6d-119">槽名稱</span><span class="sxs-lookup"><span data-stu-id="f4d6d-119">Slot Name</span></span>

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

### <span data-ttu-id="f4d6d-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f4d6d-120">-WebApp</span></span>
<span data-ttu-id="f4d6d-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="f4d6d-121">WebApp Name</span></span>

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

### <span data-ttu-id="f4d6d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d6d-122">CommonParameters</span></span>
<span data-ttu-id="f4d6d-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4d6d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d6d-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4d6d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d6d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f4d6d-125">INPUTS</span></span>

### <span data-ttu-id="f4d6d-126">網站地圖</span><span class="sxs-lookup"><span data-stu-id="f4d6d-126">Site</span></span>
<span data-ttu-id="f4d6d-127">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f4d6d-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f4d6d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f4d6d-128">OUTPUTS</span></span>

### <span data-ttu-id="f4d6d-129">WebApps WebApps. AzureWebAppBackupConfiguration （）</span><span class="sxs-lookup"><span data-stu-id="f4d6d-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f4d6d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f4d6d-130">NOTES</span></span>

## <span data-ttu-id="f4d6d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4d6d-131">RELATED LINKS</span></span>

