---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: eeaeb43083a2b125147df5d91516b71bdff377a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453964"
---
# <span data-ttu-id="d25bb-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d25bb-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="d25bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d25bb-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d25bb-103">句法</span><span class="sxs-lookup"><span data-stu-id="d25bb-103">SYNTAX</span></span>

### <span data-ttu-id="d25bb-104">S1</span><span class="sxs-lookup"><span data-stu-id="d25bb-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25bb-105">S2</span><span class="sxs-lookup"><span data-stu-id="d25bb-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d25bb-106">說明</span><span class="sxs-lookup"><span data-stu-id="d25bb-106">DESCRIPTION</span></span>
<span data-ttu-id="d25bb-107">**AzureRmWebAppSlot** Cmdlet 會移除 Azure Web App 槽，前提是資源群組和 Web 應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="d25bb-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="d25bb-108">這個 Cmdlet 預設會同時移除所有的槽與躍點數。</span><span class="sxs-lookup"><span data-stu-id="d25bb-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="d25bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="d25bb-109">EXAMPLES</span></span>

### <span data-ttu-id="d25bb-110">範例1：移除 Web 應用程式槽</span><span class="sxs-lookup"><span data-stu-id="d25bb-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="d25bb-111">這個命令會移除與屬於名為 Default-Web WestUS 之資源群組的 Web App ContosoSite 相關聯的槽 Slot001。</span><span class="sxs-lookup"><span data-stu-id="d25bb-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d25bb-112">參數</span><span class="sxs-lookup"><span data-stu-id="d25bb-112">PARAMETERS</span></span>

### <span data-ttu-id="d25bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25bb-113">-DefaultProfile</span></span>
<span data-ttu-id="d25bb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d25bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d25bb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d25bb-115">-Force</span></span>
<span data-ttu-id="d25bb-116">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="d25bb-116">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25bb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d25bb-117">-Name</span></span>
<span data-ttu-id="d25bb-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="d25bb-118">WebApp Name</span></span>

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

### <span data-ttu-id="d25bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="d25bb-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d25bb-120">Resource Group Name</span></span>

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

### <span data-ttu-id="d25bb-121">-槽</span><span class="sxs-lookup"><span data-stu-id="d25bb-121">-Slot</span></span>
<span data-ttu-id="d25bb-122">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="d25bb-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d25bb-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d25bb-123">-WebApp</span></span>
<span data-ttu-id="d25bb-124">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="d25bb-124">WebApp Object</span></span>

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

### <span data-ttu-id="d25bb-125">-確認</span><span class="sxs-lookup"><span data-stu-id="d25bb-125">-Confirm</span></span>
<span data-ttu-id="d25bb-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d25bb-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25bb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25bb-127">-WhatIf</span></span>
<span data-ttu-id="d25bb-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d25bb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d25bb-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d25bb-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="d25bb-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d25bb-130">-AsJob</span></span>
<span data-ttu-id="d25bb-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d25bb-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25bb-132">CommonParameters</span></span>
<span data-ttu-id="d25bb-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d25bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25bb-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d25bb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25bb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d25bb-135">INPUTS</span></span>

### <span data-ttu-id="d25bb-136">網站地圖</span><span class="sxs-lookup"><span data-stu-id="d25bb-136">Site</span></span>
<span data-ttu-id="d25bb-137">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d25bb-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d25bb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d25bb-138">OUTPUTS</span></span>

### <span data-ttu-id="d25bb-139">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d25bb-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d25bb-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d25bb-140">NOTES</span></span>

## <span data-ttu-id="d25bb-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d25bb-141">RELATED LINKS</span></span>

[<span data-ttu-id="d25bb-142">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d25bb-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="d25bb-143">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d25bb-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="d25bb-144">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d25bb-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="d25bb-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d25bb-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="d25bb-146">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d25bb-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="d25bb-147">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d25bb-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="d25bb-148">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="d25bb-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
