---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: a9a879386bdbc22eef3094e2f1d0cf19cd42cc45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446688"
---
# <span data-ttu-id="210b1-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="210b1-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="210b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="210b1-102">SYNOPSIS</span></span>
<span data-ttu-id="210b1-103">移除 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="210b1-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="210b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="210b1-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="210b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="210b1-105">DESCRIPTION</span></span>
<span data-ttu-id="210b1-106">AzureRmRedisCache Cmdlet 會移除 Azure Redis 快 **取** 。</span><span class="sxs-lookup"><span data-stu-id="210b1-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="210b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="210b1-107">EXAMPLES</span></span>

### <span data-ttu-id="210b1-108">範例1：移除 Redis 快取並傳回結果</span><span class="sxs-lookup"><span data-stu-id="210b1-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="210b1-109">這個命令會移除 Redis 快取，並顯示操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="210b1-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="210b1-110">範例2：移除 Redis 快取，不會顯示結果</span><span class="sxs-lookup"><span data-stu-id="210b1-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="210b1-111">這個命令會移除 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="210b1-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="210b1-112">因為未指定 *PassThru* 參數，所以不會顯示運算的結果。</span><span class="sxs-lookup"><span data-stu-id="210b1-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="210b1-113">參數</span><span class="sxs-lookup"><span data-stu-id="210b1-113">PARAMETERS</span></span>

### <span data-ttu-id="210b1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="210b1-114">-Force</span></span>
<span data-ttu-id="210b1-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="210b1-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="210b1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="210b1-116">-Name</span></span>
<span data-ttu-id="210b1-117">指定要移除之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="210b1-117">Specifies the name of the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="210b1-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="210b1-118">-PassThru</span></span>
<span data-ttu-id="210b1-119">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="210b1-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="210b1-120">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="210b1-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="210b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="210b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="210b1-122">指定包含要移除之 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="210b1-122">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="210b1-123">-確認</span><span class="sxs-lookup"><span data-stu-id="210b1-123">-Confirm</span></span>
<span data-ttu-id="210b1-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="210b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="210b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="210b1-125">-WhatIf</span></span>
<span data-ttu-id="210b1-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="210b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="210b1-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="210b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="210b1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210b1-128">-DefaultProfile</span></span>
<span data-ttu-id="210b1-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="210b1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="210b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210b1-130">CommonParameters</span></span>
<span data-ttu-id="210b1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="210b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210b1-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="210b1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210b1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="210b1-133">INPUTS</span></span>

### <span data-ttu-id="210b1-134">所有</span><span class="sxs-lookup"><span data-stu-id="210b1-134">None</span></span>
<span data-ttu-id="210b1-135">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="210b1-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="210b1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="210b1-136">OUTPUTS</span></span>

### <span data-ttu-id="210b1-137">布林值</span><span class="sxs-lookup"><span data-stu-id="210b1-137">Boolean</span></span>
<span data-ttu-id="210b1-138">如果沒有發生任何例外，則傳回 $True。</span><span class="sxs-lookup"><span data-stu-id="210b1-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="210b1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="210b1-139">NOTES</span></span>

## <span data-ttu-id="210b1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="210b1-140">RELATED LINKS</span></span>

[<span data-ttu-id="210b1-141">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="210b1-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="210b1-142">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="210b1-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="210b1-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="210b1-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


