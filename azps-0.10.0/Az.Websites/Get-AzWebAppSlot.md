---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794983"
---
# <span data-ttu-id="d743e-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d743e-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="d743e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d743e-102">SYNOPSIS</span></span>
<span data-ttu-id="d743e-103">取得 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="d743e-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="d743e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d743e-104">SYNTAX</span></span>

### <span data-ttu-id="d743e-105">S1</span><span class="sxs-lookup"><span data-stu-id="d743e-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d743e-106">S2</span><span class="sxs-lookup"><span data-stu-id="d743e-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d743e-107">說明</span><span class="sxs-lookup"><span data-stu-id="d743e-107">DESCRIPTION</span></span>
<span data-ttu-id="d743e-108">**AzWebAppSlot** Cmdlet 會取得 Azure Web App 槽的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d743e-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="d743e-109">示例</span><span class="sxs-lookup"><span data-stu-id="d743e-109">EXAMPLES</span></span>

### <span data-ttu-id="d743e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d743e-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="d743e-111">這個命令會從屬於資源群組 Default-Web-WestUS 之名為 WebAppStandard 的 Web App 取得名為 Slot001 的槽。</span><span class="sxs-lookup"><span data-stu-id="d743e-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d743e-112">參數</span><span class="sxs-lookup"><span data-stu-id="d743e-112">PARAMETERS</span></span>

### <span data-ttu-id="d743e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d743e-113">-DefaultProfile</span></span>
<span data-ttu-id="d743e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d743e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d743e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d743e-115">-Name</span></span>
<span data-ttu-id="d743e-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="d743e-116">WebApp Name</span></span>

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

### <span data-ttu-id="d743e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d743e-117">-ResourceGroupName</span></span>
<span data-ttu-id="d743e-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d743e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d743e-119">-槽</span><span class="sxs-lookup"><span data-stu-id="d743e-119">-Slot</span></span>
<span data-ttu-id="d743e-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="d743e-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d743e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d743e-121">-WebApp</span></span>
<span data-ttu-id="d743e-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="d743e-122">WebApp Object</span></span>

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

### <span data-ttu-id="d743e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d743e-123">CommonParameters</span></span>
<span data-ttu-id="d743e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d743e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d743e-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d743e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d743e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d743e-126">INPUTS</span></span>

### <span data-ttu-id="d743e-127">網站地圖</span><span class="sxs-lookup"><span data-stu-id="d743e-127">Site</span></span>
<span data-ttu-id="d743e-128">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d743e-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d743e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d743e-129">OUTPUTS</span></span>

## <span data-ttu-id="d743e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d743e-130">NOTES</span></span>

## <span data-ttu-id="d743e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d743e-131">RELATED LINKS</span></span>

[<span data-ttu-id="d743e-132">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d743e-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="d743e-133">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d743e-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="d743e-134">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d743e-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="d743e-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d743e-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="d743e-136">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d743e-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="d743e-137">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d743e-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="d743e-138">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d743e-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
