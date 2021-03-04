---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: 1d9b11aa7c259a3534b76a1d1ef011671c7f1142
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917653"
---
# <span data-ttu-id="10c18-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="10c18-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="10c18-102">簡介</span><span class="sxs-lookup"><span data-stu-id="10c18-102">SYNOPSIS</span></span>
<span data-ttu-id="10c18-103">重新產生 Redis Cache 的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="10c18-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="10c18-104">語法</span><span class="sxs-lookup"><span data-stu-id="10c18-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c18-105">描述</span><span class="sxs-lookup"><span data-stu-id="10c18-105">DESCRIPTION</span></span>
<span data-ttu-id="10c18-106">**New-AzRedisCacheKey** Cmdlet 會重新產生 Azure Redis Cache 的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="10c18-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="10c18-107">例子</span><span class="sxs-lookup"><span data-stu-id="10c18-107">EXAMPLES</span></span>

### <span data-ttu-id="10c18-108">範例 1：重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="10c18-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="10c18-109">此命令會重新產生 Redis Cache 的主鍵。</span><span class="sxs-lookup"><span data-stu-id="10c18-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="10c18-110">範例 2：重新產生次要金鑰</span><span class="sxs-lookup"><span data-stu-id="10c18-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="10c18-111">此命令會重新產生 Redis Cache 的次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="10c18-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="10c18-112">參數</span><span class="sxs-lookup"><span data-stu-id="10c18-112">PARAMETERS</span></span>

### <span data-ttu-id="10c18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c18-113">-DefaultProfile</span></span>
<span data-ttu-id="10c18-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="10c18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10c18-115">-強制</span><span class="sxs-lookup"><span data-stu-id="10c18-115">-Force</span></span>
<span data-ttu-id="10c18-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="10c18-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10c18-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="10c18-117">-KeyType</span></span>
<span data-ttu-id="10c18-118">指定要重新產生主要或次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="10c18-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="10c18-119">有效的值為：主要、次要。</span><span class="sxs-lookup"><span data-stu-id="10c18-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c18-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="10c18-120">-Name</span></span>
<span data-ttu-id="10c18-121">指定 Redis Cache 的名稱。</span><span class="sxs-lookup"><span data-stu-id="10c18-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="10c18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c18-122">-ResourceGroupName</span></span>
<span data-ttu-id="10c18-123">指定包含 Redis Cache 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="10c18-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="10c18-124">-確認</span><span class="sxs-lookup"><span data-stu-id="10c18-124">-Confirm</span></span>
<span data-ttu-id="10c18-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="10c18-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10c18-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c18-126">-WhatIf</span></span>
<span data-ttu-id="10c18-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10c18-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10c18-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10c18-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10c18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c18-129">CommonParameters</span></span>
<span data-ttu-id="10c18-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="10c18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c18-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="10c18-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c18-132">輸入</span><span class="sxs-lookup"><span data-stu-id="10c18-132">INPUTS</span></span>

### <span data-ttu-id="10c18-133">System.String</span><span class="sxs-lookup"><span data-stu-id="10c18-133">System.String</span></span>

## <span data-ttu-id="10c18-134">輸出</span><span class="sxs-lookup"><span data-stu-id="10c18-134">OUTPUTS</span></span>

### <span data-ttu-id="10c18-135">Microsoft.Azure.management.Redis.models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="10c18-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="10c18-136">筆記</span><span class="sxs-lookup"><span data-stu-id="10c18-136">NOTES</span></span>

## <span data-ttu-id="10c18-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="10c18-137">RELATED LINKS</span></span>

[<span data-ttu-id="10c18-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="10c18-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


