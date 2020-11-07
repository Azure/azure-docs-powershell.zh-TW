---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 0e1c1b9a2aa20546db1306b47b54b18c2b0cd99e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801513"
---
# <span data-ttu-id="eca57-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca57-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="eca57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eca57-102">SYNOPSIS</span></span>
<span data-ttu-id="eca57-103">停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="eca57-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eca57-104">句法</span><span class="sxs-lookup"><span data-stu-id="eca57-104">SYNTAX</span></span>

### <span data-ttu-id="eca57-105">S1</span><span class="sxs-lookup"><span data-stu-id="eca57-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eca57-106">S2</span><span class="sxs-lookup"><span data-stu-id="eca57-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eca57-107">說明</span><span class="sxs-lookup"><span data-stu-id="eca57-107">DESCRIPTION</span></span>
<span data-ttu-id="eca57-108">**AzureRmWebApp** Cmdlet 會停止 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="eca57-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="eca57-109">示例</span><span class="sxs-lookup"><span data-stu-id="eca57-109">EXAMPLES</span></span>

### <span data-ttu-id="eca57-110">範例1：停止 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="eca57-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="eca57-111">這個命令會停止屬於名為「預設-Web-WestUS」資源群組的名為 ContosoWebApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="eca57-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="eca57-112">參數</span><span class="sxs-lookup"><span data-stu-id="eca57-112">PARAMETERS</span></span>

### <span data-ttu-id="eca57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca57-113">-DefaultProfile</span></span>
<span data-ttu-id="eca57-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eca57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eca57-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eca57-115">-Name</span></span>
<span data-ttu-id="eca57-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="eca57-116">WebApp Name</span></span>

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

### <span data-ttu-id="eca57-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca57-117">-ResourceGroupName</span></span>
<span data-ttu-id="eca57-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="eca57-118">Resource Group Name</span></span>

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

### <span data-ttu-id="eca57-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eca57-119">-WebApp</span></span>
<span data-ttu-id="eca57-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="eca57-120">WebApp Object</span></span>

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

### <span data-ttu-id="eca57-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca57-121">CommonParameters</span></span>
<span data-ttu-id="eca57-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eca57-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca57-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eca57-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca57-124">輸入</span><span class="sxs-lookup"><span data-stu-id="eca57-124">INPUTS</span></span>

### <span data-ttu-id="eca57-125">網站地圖</span><span class="sxs-lookup"><span data-stu-id="eca57-125">Site</span></span>
<span data-ttu-id="eca57-126">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="eca57-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eca57-127">輸出</span><span class="sxs-lookup"><span data-stu-id="eca57-127">OUTPUTS</span></span>

## <span data-ttu-id="eca57-128">筆記</span><span class="sxs-lookup"><span data-stu-id="eca57-128">NOTES</span></span>

## <span data-ttu-id="eca57-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="eca57-129">RELATED LINKS</span></span>

[<span data-ttu-id="eca57-130">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca57-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="eca57-131">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca57-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="eca57-132">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca57-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="eca57-133">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca57-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="eca57-134">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="eca57-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


