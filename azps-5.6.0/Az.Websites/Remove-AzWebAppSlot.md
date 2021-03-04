---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: cca1cc480f529c49f679930d9d88f39f69f6e966
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909869"
---
# <span data-ttu-id="91097-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91097-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="91097-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91097-102">SYNOPSIS</span></span>

## <span data-ttu-id="91097-103">語法</span><span class="sxs-lookup"><span data-stu-id="91097-103">SYNTAX</span></span>

### <span data-ttu-id="91097-104">S1</span><span class="sxs-lookup"><span data-stu-id="91097-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91097-105">S2</span><span class="sxs-lookup"><span data-stu-id="91097-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91097-106">描述</span><span class="sxs-lookup"><span data-stu-id="91097-106">DESCRIPTION</span></span>
<span data-ttu-id="91097-107">**Remove-AzWebAppSlot** Cmdlet 會移除提供資源群組和 Web App 名稱的 Azure Web App Slot。</span><span class="sxs-lookup"><span data-stu-id="91097-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="91097-108">此 Cmdlet 預設也會移除所有插槽和度量。</span><span class="sxs-lookup"><span data-stu-id="91097-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="91097-109">例子</span><span class="sxs-lookup"><span data-stu-id="91097-109">EXAMPLES</span></span>

### <span data-ttu-id="91097-110">範例 1：移除 Web App Slot</span><span class="sxs-lookup"><span data-stu-id="91097-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="91097-111">此命令會移除與屬於 Default-Web-WestUS 資源群組的 Web App ContosoSite 相關聯的 Slot。</span><span class="sxs-lookup"><span data-stu-id="91097-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="91097-112">參數</span><span class="sxs-lookup"><span data-stu-id="91097-112">PARAMETERS</span></span>

### <span data-ttu-id="91097-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91097-113">-AsJob</span></span>
<span data-ttu-id="91097-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="91097-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91097-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91097-115">-DefaultProfile</span></span>
<span data-ttu-id="91097-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="91097-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91097-117">-強制</span><span class="sxs-lookup"><span data-stu-id="91097-117">-Force</span></span>
<span data-ttu-id="91097-118">強制移除選項</span><span class="sxs-lookup"><span data-stu-id="91097-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="91097-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="91097-119">-Name</span></span>
<span data-ttu-id="91097-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="91097-120">WebApp Name</span></span>

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

### <span data-ttu-id="91097-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91097-121">-ResourceGroupName</span></span>
<span data-ttu-id="91097-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="91097-122">Resource Group Name</span></span>

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

### <span data-ttu-id="91097-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="91097-123">-Slot</span></span>
<span data-ttu-id="91097-124">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="91097-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="91097-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="91097-125">-WebApp</span></span>
<span data-ttu-id="91097-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="91097-126">WebApp Object</span></span>

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

### <span data-ttu-id="91097-127">-確認</span><span class="sxs-lookup"><span data-stu-id="91097-127">-Confirm</span></span>
<span data-ttu-id="91097-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="91097-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91097-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91097-129">-WhatIf</span></span>
<span data-ttu-id="91097-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91097-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91097-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91097-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91097-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91097-132">CommonParameters</span></span>
<span data-ttu-id="91097-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91097-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91097-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="91097-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91097-135">輸入</span><span class="sxs-lookup"><span data-stu-id="91097-135">INPUTS</span></span>

### <span data-ttu-id="91097-136">System.String</span><span class="sxs-lookup"><span data-stu-id="91097-136">System.String</span></span>

### <span data-ttu-id="91097-137">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="91097-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="91097-138">輸出</span><span class="sxs-lookup"><span data-stu-id="91097-138">OUTPUTS</span></span>

### <span data-ttu-id="91097-139">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="91097-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="91097-140">筆記</span><span class="sxs-lookup"><span data-stu-id="91097-140">NOTES</span></span>

## <span data-ttu-id="91097-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="91097-141">RELATED LINKS</span></span>

[<span data-ttu-id="91097-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91097-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="91097-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91097-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="91097-144">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91097-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="91097-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91097-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="91097-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91097-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="91097-147">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="91097-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="91097-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="91097-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
