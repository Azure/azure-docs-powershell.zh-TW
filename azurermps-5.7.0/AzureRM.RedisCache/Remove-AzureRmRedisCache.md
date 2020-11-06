---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 4e49fbd2ac2604dab09d79255e7134fee02afd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448593"
---
# <span data-ttu-id="4cd69-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cd69-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="4cd69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cd69-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd69-103">移除 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4cd69-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cd69-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cd69-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd69-105">說明</span><span class="sxs-lookup"><span data-stu-id="4cd69-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd69-106">AzureRmRedisCache Cmdlet 會移除 Azure Redis 快 **取** 。</span><span class="sxs-lookup"><span data-stu-id="4cd69-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="4cd69-107">示例</span><span class="sxs-lookup"><span data-stu-id="4cd69-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd69-108">範例1：移除 Redis 快取並傳回結果</span><span class="sxs-lookup"><span data-stu-id="4cd69-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="4cd69-109">這個命令會移除 Redis 快取，並顯示操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="4cd69-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="4cd69-110">範例2：移除 Redis 快取，不會顯示結果</span><span class="sxs-lookup"><span data-stu-id="4cd69-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="4cd69-111">這個命令會移除 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="4cd69-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="4cd69-112">因為未指定 *PassThru* 參數，所以不會顯示運算的結果。</span><span class="sxs-lookup"><span data-stu-id="4cd69-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="4cd69-113">參數</span><span class="sxs-lookup"><span data-stu-id="4cd69-113">PARAMETERS</span></span>

### <span data-ttu-id="4cd69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd69-114">-DefaultProfile</span></span>
<span data-ttu-id="4cd69-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cd69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cd69-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4cd69-116">-Force</span></span>
<span data-ttu-id="4cd69-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4cd69-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cd69-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cd69-118">-Name</span></span>
<span data-ttu-id="4cd69-119">指定要移除之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cd69-119">Specifies the name of the Redis Cache to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd69-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cd69-120">-PassThru</span></span>
<span data-ttu-id="4cd69-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="4cd69-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4cd69-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="4cd69-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4cd69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd69-123">-ResourceGroupName</span></span>
<span data-ttu-id="4cd69-124">指定包含要移除之 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cd69-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd69-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4cd69-125">-Confirm</span></span>
<span data-ttu-id="4cd69-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cd69-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd69-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd69-127">-WhatIf</span></span>
<span data-ttu-id="4cd69-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cd69-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd69-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cd69-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd69-130">CommonParameters</span></span>
<span data-ttu-id="4cd69-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cd69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd69-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cd69-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd69-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4cd69-133">INPUTS</span></span>

### <span data-ttu-id="4cd69-134">所有</span><span class="sxs-lookup"><span data-stu-id="4cd69-134">None</span></span>
<span data-ttu-id="4cd69-135">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="4cd69-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="4cd69-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4cd69-136">OUTPUTS</span></span>

### <span data-ttu-id="4cd69-137">布林值</span><span class="sxs-lookup"><span data-stu-id="4cd69-137">Boolean</span></span>
<span data-ttu-id="4cd69-138">如果沒有發生任何例外，則傳回 $True。</span><span class="sxs-lookup"><span data-stu-id="4cd69-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="4cd69-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4cd69-139">NOTES</span></span>

## <span data-ttu-id="4cd69-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cd69-140">RELATED LINKS</span></span>

[<span data-ttu-id="4cd69-141">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cd69-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="4cd69-142">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cd69-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="4cd69-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4cd69-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


