---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141910"
---
# <span data-ttu-id="c90c7-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c90c7-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="c90c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c90c7-102">SYNOPSIS</span></span>
<span data-ttu-id="c90c7-103">移除 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="c90c7-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="c90c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="c90c7-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c90c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="c90c7-105">DESCRIPTION</span></span>
<span data-ttu-id="c90c7-106">AzRedisCache Cmdlet 會移除 Azure Redis 快 **取** 。</span><span class="sxs-lookup"><span data-stu-id="c90c7-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="c90c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="c90c7-107">EXAMPLES</span></span>

### <span data-ttu-id="c90c7-108">範例1：移除 Redis 快取並傳回結果</span><span class="sxs-lookup"><span data-stu-id="c90c7-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="c90c7-109">這個命令會移除 Redis 快取，並顯示操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="c90c7-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="c90c7-110">範例2：移除 Redis 快取，不會顯示結果</span><span class="sxs-lookup"><span data-stu-id="c90c7-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="c90c7-111">這個命令會移除 Redis 快取。</span><span class="sxs-lookup"><span data-stu-id="c90c7-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="c90c7-112">因為未指定 *PassThru* 參數，所以不會顯示運算的結果。</span><span class="sxs-lookup"><span data-stu-id="c90c7-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="c90c7-113">參數</span><span class="sxs-lookup"><span data-stu-id="c90c7-113">PARAMETERS</span></span>

### <span data-ttu-id="c90c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90c7-114">-DefaultProfile</span></span>
<span data-ttu-id="c90c7-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c90c7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c90c7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c90c7-116">-Force</span></span>
<span data-ttu-id="c90c7-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c90c7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c90c7-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c90c7-118">-Name</span></span>
<span data-ttu-id="c90c7-119">指定要移除之 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="c90c7-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="c90c7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c90c7-120">-PassThru</span></span>
<span data-ttu-id="c90c7-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c90c7-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c90c7-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c90c7-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c90c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c90c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="c90c7-124">指定包含要移除之 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c90c7-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c90c7-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c90c7-125">-Confirm</span></span>
<span data-ttu-id="c90c7-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c90c7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c90c7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c90c7-127">-WhatIf</span></span>
<span data-ttu-id="c90c7-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c90c7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c90c7-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c90c7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c90c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90c7-130">CommonParameters</span></span>
<span data-ttu-id="c90c7-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c90c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c90c7-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c90c7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90c7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c90c7-133">INPUTS</span></span>

### <span data-ttu-id="c90c7-134">System.object</span><span class="sxs-lookup"><span data-stu-id="c90c7-134">System.String</span></span>

## <span data-ttu-id="c90c7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c90c7-135">OUTPUTS</span></span>

### <span data-ttu-id="c90c7-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c90c7-136">System.Boolean</span></span>

## <span data-ttu-id="c90c7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c90c7-137">NOTES</span></span>

## <span data-ttu-id="c90c7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c90c7-138">RELATED LINKS</span></span>

[<span data-ttu-id="c90c7-139">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c90c7-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c90c7-140">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c90c7-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c90c7-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c90c7-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


