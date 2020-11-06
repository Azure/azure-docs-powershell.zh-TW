---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448226"
---
# <span data-ttu-id="43ab3-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43ab3-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="43ab3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="43ab3-103">刪除 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="43ab3-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43ab3-104">句法</span><span class="sxs-lookup"><span data-stu-id="43ab3-104">SYNTAX</span></span>

### <span data-ttu-id="43ab3-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="43ab3-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ab3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="43ab3-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43ab3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="43ab3-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ab3-108">說明</span><span class="sxs-lookup"><span data-stu-id="43ab3-108">DESCRIPTION</span></span>
<span data-ttu-id="43ab3-109">刪除即時網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="43ab3-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="43ab3-110">在此動作之後，使用者將無法在已刪除原則內設定的 Vm 上要求暫時的網路連線。</span><span class="sxs-lookup"><span data-stu-id="43ab3-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="43ab3-111">示例</span><span class="sxs-lookup"><span data-stu-id="43ab3-111">EXAMPLES</span></span>

### <span data-ttu-id="43ab3-112">範例1</span><span class="sxs-lookup"><span data-stu-id="43ab3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="43ab3-113">刪除即時網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="43ab3-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="43ab3-114">參數</span><span class="sxs-lookup"><span data-stu-id="43ab3-114">PARAMETERS</span></span>

### <span data-ttu-id="43ab3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ab3-115">-DefaultProfile</span></span>
<span data-ttu-id="43ab3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43ab3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43ab3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43ab3-117">-InputObject</span></span>
<span data-ttu-id="43ab3-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="43ab3-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43ab3-119">-位置</span><span class="sxs-lookup"><span data-stu-id="43ab3-119">-Location</span></span>
<span data-ttu-id="43ab3-120">位於.</span><span class="sxs-lookup"><span data-stu-id="43ab3-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ab3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="43ab3-121">-Name</span></span>
<span data-ttu-id="43ab3-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="43ab3-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ab3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43ab3-123">-PassThru</span></span>
<span data-ttu-id="43ab3-124">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="43ab3-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="43ab3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ab3-125">-ResourceGroupName</span></span>
<span data-ttu-id="43ab3-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="43ab3-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ab3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43ab3-127">-ResourceId</span></span>
<span data-ttu-id="43ab3-128">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="43ab3-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ab3-129">-確認</span><span class="sxs-lookup"><span data-stu-id="43ab3-129">-Confirm</span></span>
<span data-ttu-id="43ab3-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43ab3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ab3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ab3-131">-WhatIf</span></span>
<span data-ttu-id="43ab3-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43ab3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43ab3-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43ab3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ab3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ab3-134">CommonParameters</span></span>
<span data-ttu-id="43ab3-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43ab3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ab3-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43ab3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ab3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="43ab3-137">INPUTS</span></span>

### <span data-ttu-id="43ab3-138">System.object</span><span class="sxs-lookup"><span data-stu-id="43ab3-138">System.String</span></span>
<span data-ttu-id="43ab3-139">PSRemoveJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （）</span><span class="sxs-lookup"><span data-stu-id="43ab3-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="43ab3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="43ab3-140">OUTPUTS</span></span>

### <span data-ttu-id="43ab3-141">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="43ab3-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="43ab3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="43ab3-142">NOTES</span></span>

## <span data-ttu-id="43ab3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="43ab3-143">RELATED LINKS</span></span>
