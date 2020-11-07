---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: ad3ff3dbd5589a890ecf7649c9a9b66843b8b444
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802157"
---
# <span data-ttu-id="76c32-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76c32-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="76c32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76c32-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c32-103">句法</span><span class="sxs-lookup"><span data-stu-id="76c32-103">SYNTAX</span></span>

### <span data-ttu-id="76c32-104">S1</span><span class="sxs-lookup"><span data-stu-id="76c32-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c32-105">S2</span><span class="sxs-lookup"><span data-stu-id="76c32-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c32-106">說明</span><span class="sxs-lookup"><span data-stu-id="76c32-106">DESCRIPTION</span></span>
<span data-ttu-id="76c32-107">**Restart AzureRmWebAppSlot** Cmdlet 會停止，然後啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="76c32-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="76c32-108">如果 Web 應用程式槽處於停止狀態，請使用 Start-AzureRmWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76c32-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="76c32-109">示例</span><span class="sxs-lookup"><span data-stu-id="76c32-109">EXAMPLES</span></span>

### <span data-ttu-id="76c32-110">範例1</span><span class="sxs-lookup"><span data-stu-id="76c32-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="76c32-111">這個命令會重新開機與資源群組 Slot001 相關聯之 web app ContosoWebApp 的槽，其預設為 Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="76c32-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="76c32-112">參數</span><span class="sxs-lookup"><span data-stu-id="76c32-112">PARAMETERS</span></span>

### <span data-ttu-id="76c32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c32-113">-DefaultProfile</span></span>
<span data-ttu-id="76c32-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76c32-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c32-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="76c32-115">-Name</span></span>
<span data-ttu-id="76c32-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="76c32-116">WebApp Name</span></span>

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

### <span data-ttu-id="76c32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c32-117">-ResourceGroupName</span></span>
<span data-ttu-id="76c32-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="76c32-118">Resource Group Name</span></span>

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

### <span data-ttu-id="76c32-119">-槽</span><span class="sxs-lookup"><span data-stu-id="76c32-119">-Slot</span></span>
<span data-ttu-id="76c32-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="76c32-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="76c32-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="76c32-121">-WebApp</span></span>
<span data-ttu-id="76c32-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="76c32-122">WebApp Object</span></span>

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

### <span data-ttu-id="76c32-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c32-123">CommonParameters</span></span>
<span data-ttu-id="76c32-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76c32-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c32-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76c32-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c32-126">輸入</span><span class="sxs-lookup"><span data-stu-id="76c32-126">INPUTS</span></span>

### <span data-ttu-id="76c32-127">網站地圖</span><span class="sxs-lookup"><span data-stu-id="76c32-127">Site</span></span>
<span data-ttu-id="76c32-128">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="76c32-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="76c32-129">輸出</span><span class="sxs-lookup"><span data-stu-id="76c32-129">OUTPUTS</span></span>

## <span data-ttu-id="76c32-130">筆記</span><span class="sxs-lookup"><span data-stu-id="76c32-130">NOTES</span></span>

## <span data-ttu-id="76c32-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="76c32-131">RELATED LINKS</span></span>

[<span data-ttu-id="76c32-132">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76c32-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="76c32-133">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76c32-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="76c32-134">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76c32-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="76c32-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76c32-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="76c32-136">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76c32-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="76c32-137">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="76c32-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="76c32-138">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="76c32-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
