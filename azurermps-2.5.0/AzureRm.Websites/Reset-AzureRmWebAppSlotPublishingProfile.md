---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802182"
---
# <span data-ttu-id="03440-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="03440-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="03440-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03440-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03440-103">句法</span><span class="sxs-lookup"><span data-stu-id="03440-103">SYNTAX</span></span>

### <span data-ttu-id="03440-104">S1</span><span class="sxs-lookup"><span data-stu-id="03440-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03440-105">S2</span><span class="sxs-lookup"><span data-stu-id="03440-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03440-106">說明</span><span class="sxs-lookup"><span data-stu-id="03440-106">DESCRIPTION</span></span>
<span data-ttu-id="03440-107">**Reset AzureRmWebAppSlotPublishingProfile** Cmdlet 會重設指定 Web App 槽的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="03440-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="03440-108">示例</span><span class="sxs-lookup"><span data-stu-id="03440-108">EXAMPLES</span></span>

### <span data-ttu-id="03440-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="03440-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="03440-110">這個命令會針對與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp，重設 slot001 之槽的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="03440-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="03440-111">參數</span><span class="sxs-lookup"><span data-stu-id="03440-111">PARAMETERS</span></span>

### <span data-ttu-id="03440-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03440-112">-DefaultProfile</span></span>
<span data-ttu-id="03440-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03440-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03440-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="03440-114">-Name</span></span>
<span data-ttu-id="03440-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="03440-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03440-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03440-116">-ResourceGroupName</span></span>
<span data-ttu-id="03440-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="03440-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03440-118">-槽</span><span class="sxs-lookup"><span data-stu-id="03440-118">-Slot</span></span>
<span data-ttu-id="03440-119">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="03440-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03440-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="03440-120">-WebApp</span></span>
<span data-ttu-id="03440-121">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="03440-121">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03440-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03440-122">CommonParameters</span></span>
<span data-ttu-id="03440-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03440-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03440-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03440-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03440-125">輸入</span><span class="sxs-lookup"><span data-stu-id="03440-125">INPUTS</span></span>

### <span data-ttu-id="03440-126">網站地圖</span><span class="sxs-lookup"><span data-stu-id="03440-126">Site</span></span>
<span data-ttu-id="03440-127">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="03440-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="03440-128">輸出</span><span class="sxs-lookup"><span data-stu-id="03440-128">OUTPUTS</span></span>

## <span data-ttu-id="03440-129">筆記</span><span class="sxs-lookup"><span data-stu-id="03440-129">NOTES</span></span>

## <span data-ttu-id="03440-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="03440-130">RELATED LINKS</span></span>

