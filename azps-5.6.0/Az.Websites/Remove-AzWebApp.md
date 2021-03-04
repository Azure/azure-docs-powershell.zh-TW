---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 1ce172ea2f1851f2f75a95a3037798ca3b3a2bf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904189"
---
# <span data-ttu-id="ff866-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff866-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="ff866-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ff866-102">SYNOPSIS</span></span>
<span data-ttu-id="ff866-103">移除 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="ff866-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="ff866-104">語法</span><span class="sxs-lookup"><span data-stu-id="ff866-104">SYNTAX</span></span>

### <span data-ttu-id="ff866-105">S1</span><span class="sxs-lookup"><span data-stu-id="ff866-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff866-106">S2</span><span class="sxs-lookup"><span data-stu-id="ff866-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff866-107">描述</span><span class="sxs-lookup"><span data-stu-id="ff866-107">DESCRIPTION</span></span>
<span data-ttu-id="ff866-108">**Remove-AzWebApp** Cmdlet 會移除提供資源群組和 Web App 名稱的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="ff866-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="ff866-109">此 Cmdlet 預設也會移除所有插槽和度量。</span><span class="sxs-lookup"><span data-stu-id="ff866-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="ff866-110">例子</span><span class="sxs-lookup"><span data-stu-id="ff866-110">EXAMPLES</span></span>

### <span data-ttu-id="ff866-111">範例 1：移除 Web App</span><span class="sxs-lookup"><span data-stu-id="ff866-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ff866-112">此命令會移除名稱為 ContosoSite 的 Azure Web App，此 App 屬於名為 Default-Web-WestUS 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ff866-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ff866-113">參數</span><span class="sxs-lookup"><span data-stu-id="ff866-113">PARAMETERS</span></span>

### <span data-ttu-id="ff866-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff866-114">-AsJob</span></span>
<span data-ttu-id="ff866-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff866-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff866-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff866-116">-DefaultProfile</span></span>
<span data-ttu-id="ff866-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff866-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff866-118">-強制</span><span class="sxs-lookup"><span data-stu-id="ff866-118">-Force</span></span>
<span data-ttu-id="ff866-119">強制移除選項</span><span class="sxs-lookup"><span data-stu-id="ff866-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ff866-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff866-120">-Name</span></span>
<span data-ttu-id="ff866-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="ff866-121">WebApp Name</span></span>

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

### <span data-ttu-id="ff866-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff866-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff866-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="ff866-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ff866-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ff866-124">-WebApp</span></span>
<span data-ttu-id="ff866-125">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="ff866-125">WebApp Object</span></span>

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

### <span data-ttu-id="ff866-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ff866-126">-Confirm</span></span>
<span data-ttu-id="ff866-127">執行 Cmdlet 之前，提示您確認。執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ff866-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff866-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff866-128">-WhatIf</span></span>
<span data-ttu-id="ff866-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff866-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff866-130">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff866-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff866-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff866-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff866-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff866-132">CommonParameters</span></span>
<span data-ttu-id="ff866-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ff866-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff866-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ff866-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff866-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ff866-135">INPUTS</span></span>

### <span data-ttu-id="ff866-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ff866-136">System.String</span></span>

### <span data-ttu-id="ff866-137">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ff866-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ff866-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ff866-138">OUTPUTS</span></span>

### <span data-ttu-id="ff866-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="ff866-139">System.Void</span></span>

## <span data-ttu-id="ff866-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ff866-140">NOTES</span></span>

## <span data-ttu-id="ff866-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff866-141">RELATED LINKS</span></span>

[<span data-ttu-id="ff866-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff866-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ff866-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff866-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ff866-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff866-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ff866-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff866-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ff866-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff866-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


