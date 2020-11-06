---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnProfile.md
ms.openlocfilehash: f564a026359042a20e5d82e34425e98f1021422b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450013"
---
# <span data-ttu-id="2bc8b-101">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8b-101">Remove-AzureRmCdnProfile</span></span>

## <span data-ttu-id="2bc8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bc8b-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc8b-103">移除 CDN 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-103">Removes a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bc8b-104">SYNTAX</span></span>

### <span data-ttu-id="2bc8b-105">欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="2bc8b-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bc8b-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="2bc8b-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc8b-107">說明</span><span class="sxs-lookup"><span data-stu-id="2bc8b-107">DESCRIPTION</span></span>
<span data-ttu-id="2bc8b-108">**AzureRmCdnProfile** Cmdlet 會將 Azure 內容傳遞網路 (CDN) 設定檔中移除。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-108">The **Remove-AzureRmCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="2bc8b-109">示例</span><span class="sxs-lookup"><span data-stu-id="2bc8b-109">EXAMPLES</span></span>

## <span data-ttu-id="2bc8b-110">參數</span><span class="sxs-lookup"><span data-stu-id="2bc8b-110">PARAMETERS</span></span>

### <span data-ttu-id="2bc8b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8b-111">-CdnProfile</span></span>
<span data-ttu-id="2bc8b-112">指定此 Cmdlet 移除的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2bc8b-113">-Force</span></span>
<span data-ttu-id="2bc8b-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2bc8b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bc8b-115">-PassThru</span></span>
<span data-ttu-id="2bc8b-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2bc8b-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2bc8b-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2bc8b-118">-ProfileName</span></span>
<span data-ttu-id="2bc8b-119">指定此 Cmdlet 移除的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-119">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc8b-120">-ResourceGroupName</span></span>
<span data-ttu-id="2bc8b-121">指定設定檔所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-121">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc8b-122">-確認</span><span class="sxs-lookup"><span data-stu-id="2bc8b-122">-Confirm</span></span>
<span data-ttu-id="2bc8b-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bc8b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc8b-124">-WhatIf</span></span>
<span data-ttu-id="2bc8b-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc8b-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bc8b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8b-127">-DefaultProfile</span></span>
<span data-ttu-id="2bc8b-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc8b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc8b-129">CommonParameters</span></span>
<span data-ttu-id="2bc8b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc8b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bc8b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc8b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2bc8b-132">INPUTS</span></span>

### <span data-ttu-id="2bc8b-133">PSProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8b-133">PSProfile</span></span>
<span data-ttu-id="2bc8b-134">形參 "CdnProfile" 接受管線中 "PSProfile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2bc8b-134">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="2bc8b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2bc8b-135">OUTPUTS</span></span>

### <span data-ttu-id="2bc8b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="2bc8b-136">System.Boolean</span></span>

## <span data-ttu-id="2bc8b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2bc8b-137">NOTES</span></span>

## <span data-ttu-id="2bc8b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bc8b-138">RELATED LINKS</span></span>

[<span data-ttu-id="2bc8b-139">AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8b-139">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="2bc8b-140">新-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8b-140">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="2bc8b-141">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2bc8b-141">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


