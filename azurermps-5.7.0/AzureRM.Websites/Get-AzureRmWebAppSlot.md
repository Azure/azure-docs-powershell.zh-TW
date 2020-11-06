---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: b22dcb6518aa42104a44207e85d02dd7bab914bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445892"
---
# <span data-ttu-id="2825c-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2825c-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="2825c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2825c-102">SYNOPSIS</span></span>
<span data-ttu-id="2825c-103">取得 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="2825c-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2825c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2825c-104">SYNTAX</span></span>

### <span data-ttu-id="2825c-105">S1</span><span class="sxs-lookup"><span data-stu-id="2825c-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2825c-106">S2</span><span class="sxs-lookup"><span data-stu-id="2825c-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2825c-107">說明</span><span class="sxs-lookup"><span data-stu-id="2825c-107">DESCRIPTION</span></span>
<span data-ttu-id="2825c-108">**AzureRmWebAppSlot** Cmdlet 會取得 Azure Web App 槽的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2825c-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="2825c-109">示例</span><span class="sxs-lookup"><span data-stu-id="2825c-109">EXAMPLES</span></span>

### <span data-ttu-id="2825c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2825c-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="2825c-111">這個命令會從屬於資源群組 Default-Web-WestUS 之名為 WebAppStandard 的 Web App 取得名為 Slot001 的槽。</span><span class="sxs-lookup"><span data-stu-id="2825c-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2825c-112">參數</span><span class="sxs-lookup"><span data-stu-id="2825c-112">PARAMETERS</span></span>

### <span data-ttu-id="2825c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2825c-113">-DefaultProfile</span></span>
<span data-ttu-id="2825c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2825c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2825c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2825c-115">-Name</span></span>
<span data-ttu-id="2825c-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2825c-116">WebApp Name</span></span>

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

### <span data-ttu-id="2825c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2825c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2825c-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2825c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2825c-119">-槽</span><span class="sxs-lookup"><span data-stu-id="2825c-119">-Slot</span></span>
<span data-ttu-id="2825c-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="2825c-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2825c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2825c-121">-WebApp</span></span>
<span data-ttu-id="2825c-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2825c-122">WebApp Object</span></span>

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

### <span data-ttu-id="2825c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2825c-123">CommonParameters</span></span>
<span data-ttu-id="2825c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2825c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2825c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2825c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2825c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="2825c-126">INPUTS</span></span>

### <span data-ttu-id="2825c-127">網站地圖</span><span class="sxs-lookup"><span data-stu-id="2825c-127">Site</span></span>
<span data-ttu-id="2825c-128">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2825c-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2825c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2825c-129">OUTPUTS</span></span>

## <span data-ttu-id="2825c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2825c-130">NOTES</span></span>

## <span data-ttu-id="2825c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2825c-131">RELATED LINKS</span></span>

[<span data-ttu-id="2825c-132">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2825c-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="2825c-133">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2825c-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="2825c-134">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2825c-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="2825c-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2825c-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="2825c-136">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2825c-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="2825c-137">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2825c-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="2825c-138">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2825c-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
