---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794945"
---
# <span data-ttu-id="2053b-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2053b-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="2053b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2053b-102">SYNOPSIS</span></span>

## <span data-ttu-id="2053b-103">句法</span><span class="sxs-lookup"><span data-stu-id="2053b-103">SYNTAX</span></span>

### <span data-ttu-id="2053b-104">S1</span><span class="sxs-lookup"><span data-stu-id="2053b-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2053b-105">S2</span><span class="sxs-lookup"><span data-stu-id="2053b-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2053b-106">說明</span><span class="sxs-lookup"><span data-stu-id="2053b-106">DESCRIPTION</span></span>
<span data-ttu-id="2053b-107">**Restart AzWebAppSlot** Cmdlet 會停止，然後啟動 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="2053b-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="2053b-108">如果 Web 應用程式槽處於停止狀態，請使用 Start-AzWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2053b-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="2053b-109">示例</span><span class="sxs-lookup"><span data-stu-id="2053b-109">EXAMPLES</span></span>

### <span data-ttu-id="2053b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2053b-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="2053b-111">這個命令會重新開機與資源群組 Slot001 相關聯之 web app ContosoWebApp 的槽，其預設為 Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="2053b-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2053b-112">參數</span><span class="sxs-lookup"><span data-stu-id="2053b-112">PARAMETERS</span></span>

### <span data-ttu-id="2053b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2053b-113">-DefaultProfile</span></span>
<span data-ttu-id="2053b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2053b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2053b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2053b-115">-Name</span></span>
<span data-ttu-id="2053b-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2053b-116">WebApp Name</span></span>

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

### <span data-ttu-id="2053b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2053b-117">-ResourceGroupName</span></span>
<span data-ttu-id="2053b-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2053b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2053b-119">-槽</span><span class="sxs-lookup"><span data-stu-id="2053b-119">-Slot</span></span>
<span data-ttu-id="2053b-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="2053b-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2053b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2053b-121">-WebApp</span></span>
<span data-ttu-id="2053b-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2053b-122">WebApp Object</span></span>

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

### <span data-ttu-id="2053b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2053b-123">CommonParameters</span></span>
<span data-ttu-id="2053b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2053b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2053b-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2053b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2053b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="2053b-126">INPUTS</span></span>

### <span data-ttu-id="2053b-127">網站地圖</span><span class="sxs-lookup"><span data-stu-id="2053b-127">Site</span></span>
<span data-ttu-id="2053b-128">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2053b-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2053b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2053b-129">OUTPUTS</span></span>

## <span data-ttu-id="2053b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2053b-130">NOTES</span></span>

## <span data-ttu-id="2053b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2053b-131">RELATED LINKS</span></span>

[<span data-ttu-id="2053b-132">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2053b-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2053b-133">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2053b-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="2053b-134">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2053b-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="2053b-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2053b-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="2053b-136">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2053b-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2053b-137">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2053b-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2053b-138">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2053b-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
