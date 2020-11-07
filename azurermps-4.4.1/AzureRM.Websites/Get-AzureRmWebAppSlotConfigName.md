---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 196e653447204b65c7f431e29fe76078a268dda1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625949"
---
# <span data-ttu-id="c0eb0-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="c0eb0-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="c0eb0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="c0eb0-103">取得 Web 應用程式槽配置名稱的清單</span><span class="sxs-lookup"><span data-stu-id="c0eb0-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0eb0-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0eb0-104">SYNTAX</span></span>

### <span data-ttu-id="c0eb0-105">S1</span><span class="sxs-lookup"><span data-stu-id="c0eb0-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0eb0-106">S2</span><span class="sxs-lookup"><span data-stu-id="c0eb0-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0eb0-107">說明</span><span class="sxs-lookup"><span data-stu-id="c0eb0-107">DESCRIPTION</span></span>
<span data-ttu-id="c0eb0-108">**AzureRmWebAppSlotConfigName** Cmdlet 會檢索應用程式設定清單，以及目前標示為槽設定的連接字串名稱</span><span class="sxs-lookup"><span data-stu-id="c0eb0-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="c0eb0-109">示例</span><span class="sxs-lookup"><span data-stu-id="c0eb0-109">EXAMPLES</span></span>

### <span data-ttu-id="c0eb0-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="c0eb0-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c0eb0-111">這個命令會取得與資源群組預設的 Web 應用程式相關的 App 設定和連線字串（與資源群組預設的 Web WestUS 有關）。</span><span class="sxs-lookup"><span data-stu-id="c0eb0-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c0eb0-112">參數</span><span class="sxs-lookup"><span data-stu-id="c0eb0-112">PARAMETERS</span></span>

### <span data-ttu-id="c0eb0-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0eb0-113">-Name</span></span>
<span data-ttu-id="c0eb0-114">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c0eb0-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0eb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0eb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0eb0-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c0eb0-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0eb0-117">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c0eb0-117">-WebApp</span></span>
<span data-ttu-id="c0eb0-118">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c0eb0-118">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0eb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0eb0-119">-DefaultProfile</span></span>
<span data-ttu-id="c0eb0-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0eb0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0eb0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0eb0-121">CommonParameters</span></span>
<span data-ttu-id="c0eb0-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0eb0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0eb0-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0eb0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0eb0-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c0eb0-124">INPUTS</span></span>

### <span data-ttu-id="c0eb0-125">網站地圖</span><span class="sxs-lookup"><span data-stu-id="c0eb0-125">Site</span></span>
<span data-ttu-id="c0eb0-126">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c0eb0-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c0eb0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c0eb0-127">OUTPUTS</span></span>

## <span data-ttu-id="c0eb0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c0eb0-128">NOTES</span></span>

## <span data-ttu-id="c0eb0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0eb0-129">RELATED LINKS</span></span>

