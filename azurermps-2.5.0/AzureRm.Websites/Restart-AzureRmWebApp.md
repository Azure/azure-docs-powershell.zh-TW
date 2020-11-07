---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 775c82585d31e223b3f769cccc458e1523f42b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801857"
---
# <span data-ttu-id="f91d3-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f91d3-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="f91d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f91d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f91d3-103">重新開機 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="f91d3-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f91d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="f91d3-104">SYNTAX</span></span>

### <span data-ttu-id="f91d3-105">S1</span><span class="sxs-lookup"><span data-stu-id="f91d3-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f91d3-106">S2</span><span class="sxs-lookup"><span data-stu-id="f91d3-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f91d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="f91d3-107">DESCRIPTION</span></span>
<span data-ttu-id="f91d3-108">**Restart AzureRmWebApp** Cmdlet 會停止，然後啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="f91d3-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="f91d3-109">如果 Web App 處於停止狀態，請使用 Start-AzureRmWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f91d3-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="f91d3-110">示例</span><span class="sxs-lookup"><span data-stu-id="f91d3-110">EXAMPLES</span></span>

### <span data-ttu-id="f91d3-111">範例1：重新開機 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="f91d3-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f91d3-112">這個命令會停止名為 ContosoSite 的 Azure Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組，然後重新開機它。</span><span class="sxs-lookup"><span data-stu-id="f91d3-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="f91d3-113">參數</span><span class="sxs-lookup"><span data-stu-id="f91d3-113">PARAMETERS</span></span>

### <span data-ttu-id="f91d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91d3-114">-DefaultProfile</span></span>
<span data-ttu-id="f91d3-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f91d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f91d3-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f91d3-116">-Name</span></span>
<span data-ttu-id="f91d3-117">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="f91d3-117">WebApp Name</span></span>

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

### <span data-ttu-id="f91d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="f91d3-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f91d3-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f91d3-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f91d3-120">-WebApp</span></span>
<span data-ttu-id="f91d3-121">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="f91d3-121">WebApp Object</span></span>

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

### <span data-ttu-id="f91d3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91d3-122">CommonParameters</span></span>
<span data-ttu-id="f91d3-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f91d3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91d3-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f91d3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91d3-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f91d3-125">INPUTS</span></span>

### <span data-ttu-id="f91d3-126">網站地圖</span><span class="sxs-lookup"><span data-stu-id="f91d3-126">Site</span></span>
<span data-ttu-id="f91d3-127">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f91d3-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f91d3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f91d3-128">OUTPUTS</span></span>

## <span data-ttu-id="f91d3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f91d3-129">NOTES</span></span>

## <span data-ttu-id="f91d3-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f91d3-130">RELATED LINKS</span></span>

[<span data-ttu-id="f91d3-131">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f91d3-131">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f91d3-132">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f91d3-132">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f91d3-133">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f91d3-133">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="f91d3-134">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f91d3-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f91d3-135">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f91d3-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


