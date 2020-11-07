---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801506"
---
# <span data-ttu-id="189e3-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="189e3-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="189e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="189e3-102">SYNOPSIS</span></span>
<span data-ttu-id="189e3-103">停止 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="189e3-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="189e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="189e3-104">SYNTAX</span></span>

### <span data-ttu-id="189e3-105">S1</span><span class="sxs-lookup"><span data-stu-id="189e3-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="189e3-106">S2</span><span class="sxs-lookup"><span data-stu-id="189e3-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="189e3-107">說明</span><span class="sxs-lookup"><span data-stu-id="189e3-107">DESCRIPTION</span></span>
<span data-ttu-id="189e3-108">**AzureRmWebAppSlot** Cmdlet 會停止 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="189e3-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="189e3-109">示例</span><span class="sxs-lookup"><span data-stu-id="189e3-109">EXAMPLES</span></span>

### <span data-ttu-id="189e3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="189e3-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="189e3-111">這個命令會停止與屬於名為「預設-Web-WestUS」之資源群組的名為 ContosoWebApp 的 Web App 相關的槽 Slot001。</span><span class="sxs-lookup"><span data-stu-id="189e3-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="189e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="189e3-112">PARAMETERS</span></span>

### <span data-ttu-id="189e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189e3-113">-DefaultProfile</span></span>
<span data-ttu-id="189e3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="189e3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="189e3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="189e3-115">-Name</span></span>
<span data-ttu-id="189e3-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="189e3-116">WebApp Name</span></span>

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

### <span data-ttu-id="189e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="189e3-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="189e3-118">Resource Group Name</span></span>

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

### <span data-ttu-id="189e3-119">-槽</span><span class="sxs-lookup"><span data-stu-id="189e3-119">-Slot</span></span>
<span data-ttu-id="189e3-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="189e3-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="189e3-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="189e3-121">-WebApp</span></span>
<span data-ttu-id="189e3-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="189e3-122">WebApp Object</span></span>

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

### <span data-ttu-id="189e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189e3-123">CommonParameters</span></span>
<span data-ttu-id="189e3-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="189e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189e3-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="189e3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189e3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="189e3-126">INPUTS</span></span>

### <span data-ttu-id="189e3-127">網站地圖</span><span class="sxs-lookup"><span data-stu-id="189e3-127">Site</span></span>
<span data-ttu-id="189e3-128">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="189e3-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="189e3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="189e3-129">OUTPUTS</span></span>

## <span data-ttu-id="189e3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="189e3-130">NOTES</span></span>

## <span data-ttu-id="189e3-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="189e3-131">RELATED LINKS</span></span>

