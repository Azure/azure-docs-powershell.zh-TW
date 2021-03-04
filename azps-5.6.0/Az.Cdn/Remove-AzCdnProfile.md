---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 904af1f1d1f6cba7bd0a44ee0811b55fef01e106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913594"
---
# <span data-ttu-id="fc49b-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fc49b-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="fc49b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc49b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc49b-103">移除 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc49b-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="fc49b-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc49b-104">SYNTAX</span></span>

### <span data-ttu-id="fc49b-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc49b-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc49b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc49b-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc49b-107">描述</span><span class="sxs-lookup"><span data-stu-id="fc49b-107">DESCRIPTION</span></span>
<span data-ttu-id="fc49b-108">**Remove-AzCdnProfile** Cmdlet 會移除 AZURE 內容傳遞網路 (CDN) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc49b-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="fc49b-109">例子</span><span class="sxs-lookup"><span data-stu-id="fc49b-109">EXAMPLES</span></span>

## <span data-ttu-id="fc49b-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc49b-110">PARAMETERS</span></span>

### <span data-ttu-id="fc49b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fc49b-111">-CdnProfile</span></span>
<span data-ttu-id="fc49b-112">指定此 Cmdlet 移除的設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc49b-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc49b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc49b-113">-DefaultProfile</span></span>
<span data-ttu-id="fc49b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fc49b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc49b-115">-強制</span><span class="sxs-lookup"><span data-stu-id="fc49b-115">-Force</span></span>
<span data-ttu-id="fc49b-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fc49b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc49b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc49b-117">-PassThru</span></span>
<span data-ttu-id="fc49b-118">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fc49b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc49b-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fc49b-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc49b-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fc49b-120">-ProfileName</span></span>
<span data-ttu-id="fc49b-121">指定此 Cmdlet 移除的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="fc49b-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc49b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc49b-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc49b-123">指定設定檔所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fc49b-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc49b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="fc49b-124">-Confirm</span></span>
<span data-ttu-id="fc49b-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fc49b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc49b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc49b-126">-WhatIf</span></span>
<span data-ttu-id="fc49b-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc49b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc49b-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc49b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc49b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc49b-129">CommonParameters</span></span>
<span data-ttu-id="fc49b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc49b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc49b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc49b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc49b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fc49b-132">INPUTS</span></span>

### <span data-ttu-id="fc49b-133">Microsoft.Azure.Commands.Cdn.models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="fc49b-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="fc49b-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc49b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc49b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fc49b-135">OUTPUTS</span></span>

### <span data-ttu-id="fc49b-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc49b-136">System.Boolean</span></span>

## <span data-ttu-id="fc49b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fc49b-137">NOTES</span></span>

## <span data-ttu-id="fc49b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc49b-138">RELATED LINKS</span></span>

[<span data-ttu-id="fc49b-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fc49b-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="fc49b-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fc49b-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="fc49b-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fc49b-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


