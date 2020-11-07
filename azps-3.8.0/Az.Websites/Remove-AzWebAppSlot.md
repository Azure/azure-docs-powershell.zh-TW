---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 88eaf66ea8584913c7816fd12be19509aec49de5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958861"
---
# <span data-ttu-id="964d9-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="964d9-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="964d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="964d9-102">SYNOPSIS</span></span>

## <span data-ttu-id="964d9-103">句法</span><span class="sxs-lookup"><span data-stu-id="964d9-103">SYNTAX</span></span>

### <span data-ttu-id="964d9-104">S1</span><span class="sxs-lookup"><span data-stu-id="964d9-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="964d9-105">S2</span><span class="sxs-lookup"><span data-stu-id="964d9-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="964d9-106">說明</span><span class="sxs-lookup"><span data-stu-id="964d9-106">DESCRIPTION</span></span>
<span data-ttu-id="964d9-107">**AzWebAppSlot** Cmdlet 會移除 Azure Web App 槽，前提是資源群組和 Web 應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="964d9-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="964d9-108">這個 Cmdlet 預設會同時移除所有的槽與躍點數。</span><span class="sxs-lookup"><span data-stu-id="964d9-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="964d9-109">示例</span><span class="sxs-lookup"><span data-stu-id="964d9-109">EXAMPLES</span></span>

### <span data-ttu-id="964d9-110">範例1：移除 Web 應用程式槽</span><span class="sxs-lookup"><span data-stu-id="964d9-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="964d9-111">這個命令會移除與屬於名為 Default-Web WestUS 之資源群組的 Web App ContosoSite 相關聯的槽 Slot001。</span><span class="sxs-lookup"><span data-stu-id="964d9-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="964d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="964d9-112">PARAMETERS</span></span>

### <span data-ttu-id="964d9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="964d9-113">-AsJob</span></span>
<span data-ttu-id="964d9-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="964d9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="964d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964d9-115">-DefaultProfile</span></span>
<span data-ttu-id="964d9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="964d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="964d9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="964d9-117">-Force</span></span>
<span data-ttu-id="964d9-118">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="964d9-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="964d9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="964d9-119">-Name</span></span>
<span data-ttu-id="964d9-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="964d9-120">WebApp Name</span></span>

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

### <span data-ttu-id="964d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="964d9-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="964d9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="964d9-123">-槽</span><span class="sxs-lookup"><span data-stu-id="964d9-123">-Slot</span></span>
<span data-ttu-id="964d9-124">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="964d9-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="964d9-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="964d9-125">-WebApp</span></span>
<span data-ttu-id="964d9-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="964d9-126">WebApp Object</span></span>

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

### <span data-ttu-id="964d9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="964d9-127">-Confirm</span></span>
<span data-ttu-id="964d9-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="964d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="964d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="964d9-129">-WhatIf</span></span>
<span data-ttu-id="964d9-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="964d9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="964d9-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="964d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="964d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964d9-132">CommonParameters</span></span>
<span data-ttu-id="964d9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="964d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964d9-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="964d9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964d9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="964d9-135">INPUTS</span></span>

### <span data-ttu-id="964d9-136">System.object</span><span class="sxs-lookup"><span data-stu-id="964d9-136">System.String</span></span>

### <span data-ttu-id="964d9-137">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="964d9-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="964d9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="964d9-138">OUTPUTS</span></span>

### <span data-ttu-id="964d9-139">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="964d9-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="964d9-140">筆記</span><span class="sxs-lookup"><span data-stu-id="964d9-140">NOTES</span></span>

## <span data-ttu-id="964d9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="964d9-141">RELATED LINKS</span></span>

[<span data-ttu-id="964d9-142">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="964d9-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="964d9-143">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="964d9-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="964d9-144">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="964d9-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="964d9-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="964d9-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="964d9-146">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="964d9-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="964d9-147">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="964d9-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="964d9-148">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="964d9-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
