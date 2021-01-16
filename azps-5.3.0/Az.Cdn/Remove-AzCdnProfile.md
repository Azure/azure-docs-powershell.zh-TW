---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446604"
---
# <span data-ttu-id="5f3d1-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5f3d1-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="5f3d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3d1-103">移除 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="5f3d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f3d1-104">SYNTAX</span></span>

### <span data-ttu-id="5f3d1-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f3d1-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f3d1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f3d1-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f3d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="5f3d1-107">DESCRIPTION</span></span>
<span data-ttu-id="5f3d1-108">**AzCdnProfile** Cmdlet 會將 Azure 內容傳遞網路 (CDN) 設定檔中移除。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="5f3d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="5f3d1-109">EXAMPLES</span></span>

## <span data-ttu-id="5f3d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="5f3d1-110">PARAMETERS</span></span>

### <span data-ttu-id="5f3d1-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5f3d1-111">-CdnProfile</span></span>
<span data-ttu-id="5f3d1-112">指定此 Cmdlet 移除的設定檔。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5f3d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f3d1-113">-DefaultProfile</span></span>
<span data-ttu-id="5f3d1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5f3d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f3d1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5f3d1-115">-Force</span></span>
<span data-ttu-id="5f3d1-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5f3d1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f3d1-117">-PassThru</span></span>
<span data-ttu-id="5f3d1-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5f3d1-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5f3d1-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5f3d1-120">-ProfileName</span></span>
<span data-ttu-id="5f3d1-121">指定此 Cmdlet 移除的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5f3d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f3d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f3d1-123">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5f3d1-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5f3d1-124">-Confirm</span></span>
<span data-ttu-id="5f3d1-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f3d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f3d1-126">-WhatIf</span></span>
<span data-ttu-id="5f3d1-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f3d1-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f3d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f3d1-129">CommonParameters</span></span>
<span data-ttu-id="5f3d1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f3d1-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5f3d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f3d1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5f3d1-132">INPUTS</span></span>

### <span data-ttu-id="5f3d1-133">PSProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5f3d1-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="5f3d1-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5f3d1-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5f3d1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5f3d1-135">OUTPUTS</span></span>

### <span data-ttu-id="5f3d1-136">System.object</span><span class="sxs-lookup"><span data-stu-id="5f3d1-136">System.Boolean</span></span>

## <span data-ttu-id="5f3d1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5f3d1-137">NOTES</span></span>

## <span data-ttu-id="5f3d1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f3d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="5f3d1-139">AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5f3d1-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="5f3d1-140">新-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5f3d1-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="5f3d1-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5f3d1-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


