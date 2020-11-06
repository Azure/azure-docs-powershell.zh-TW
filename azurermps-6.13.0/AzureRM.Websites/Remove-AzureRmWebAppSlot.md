---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449668"
---
# <span data-ttu-id="c6405-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6405-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="c6405-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6405-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6405-103">句法</span><span class="sxs-lookup"><span data-stu-id="c6405-103">SYNTAX</span></span>

### <span data-ttu-id="c6405-104">S1</span><span class="sxs-lookup"><span data-stu-id="c6405-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6405-105">S2</span><span class="sxs-lookup"><span data-stu-id="c6405-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6405-106">說明</span><span class="sxs-lookup"><span data-stu-id="c6405-106">DESCRIPTION</span></span>
<span data-ttu-id="c6405-107">**AzureRmWebAppSlot** Cmdlet 會移除 Azure Web App 槽，前提是資源群組和 Web 應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="c6405-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="c6405-108">這個 Cmdlet 預設會同時移除所有的槽與躍點數。</span><span class="sxs-lookup"><span data-stu-id="c6405-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="c6405-109">示例</span><span class="sxs-lookup"><span data-stu-id="c6405-109">EXAMPLES</span></span>

### <span data-ttu-id="c6405-110">範例1：移除 Web 應用程式槽</span><span class="sxs-lookup"><span data-stu-id="c6405-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="c6405-111">這個命令會移除與屬於名為 Default-Web WestUS 之資源群組的 Web App ContosoSite 相關聯的槽 Slot001。</span><span class="sxs-lookup"><span data-stu-id="c6405-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c6405-112">參數</span><span class="sxs-lookup"><span data-stu-id="c6405-112">PARAMETERS</span></span>

### <span data-ttu-id="c6405-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6405-113">-AsJob</span></span>
<span data-ttu-id="c6405-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c6405-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6405-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6405-115">-DefaultProfile</span></span>
<span data-ttu-id="c6405-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6405-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6405-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c6405-117">-Force</span></span>
<span data-ttu-id="c6405-118">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="c6405-118">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6405-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6405-119">-Name</span></span>
<span data-ttu-id="c6405-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c6405-120">WebApp Name</span></span>

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

### <span data-ttu-id="c6405-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6405-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6405-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c6405-122">Resource Group Name</span></span>

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

### <span data-ttu-id="c6405-123">-槽</span><span class="sxs-lookup"><span data-stu-id="c6405-123">-Slot</span></span>
<span data-ttu-id="c6405-124">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="c6405-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6405-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c6405-125">-WebApp</span></span>
<span data-ttu-id="c6405-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c6405-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6405-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c6405-127">-Confirm</span></span>
<span data-ttu-id="c6405-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6405-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6405-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6405-129">-WhatIf</span></span>
<span data-ttu-id="c6405-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6405-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6405-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6405-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6405-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6405-132">CommonParameters</span></span>
<span data-ttu-id="c6405-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6405-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6405-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6405-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6405-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c6405-135">INPUTS</span></span>

### <span data-ttu-id="c6405-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c6405-136">System.String</span></span>

### <span data-ttu-id="c6405-137">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="c6405-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c6405-138">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c6405-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c6405-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c6405-139">OUTPUTS</span></span>

### <span data-ttu-id="c6405-140">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c6405-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c6405-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c6405-141">NOTES</span></span>

## <span data-ttu-id="c6405-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6405-142">RELATED LINKS</span></span>

[<span data-ttu-id="c6405-143">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6405-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="c6405-144">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6405-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="c6405-145">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6405-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="c6405-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6405-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="c6405-147">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6405-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="c6405-148">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c6405-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="c6405-149">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c6405-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
