---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286811"
---
# <span data-ttu-id="fb3d9-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fb3d9-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="fb3d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3d9-103">刪除 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="fb3d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb3d9-104">SYNTAX</span></span>

### <span data-ttu-id="fb3d9-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3d9-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3d9-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3d9-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3d9-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3d9-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3d9-108">說明</span><span class="sxs-lookup"><span data-stu-id="fb3d9-108">DESCRIPTION</span></span>
<span data-ttu-id="fb3d9-109">**AzSecurityPartnerProvider** Cmdlet 會刪除 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fb3d9-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="fb3d9-110">示例</span><span class="sxs-lookup"><span data-stu-id="fb3d9-110">EXAMPLES</span></span>

### <span data-ttu-id="fb3d9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fb3d9-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="fb3d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="fb3d9-112">PARAMETERS</span></span>

### <span data-ttu-id="fb3d9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb3d9-113">-AsJob</span></span>
<span data-ttu-id="fb3d9-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb3d9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb3d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3d9-115">-DefaultProfile</span></span>
<span data-ttu-id="fb3d9-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fb3d9-117">-Force</span></span>
<span data-ttu-id="fb3d9-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fb3d9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb3d9-119">-Name</span></span>
<span data-ttu-id="fb3d9-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb3d9-121">-PassThru</span></span>
<span data-ttu-id="fb3d9-122">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="fb3d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="fb3d9-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb3d9-125">-ResourceId</span></span>
<span data-ttu-id="fb3d9-126">SecurityPartnerProvider 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d9-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fb3d9-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="fb3d9-128">SecurityPartnerProvider 輸入物件。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3d9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fb3d9-129">-Confirm</span></span>
<span data-ttu-id="fb3d9-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3d9-131">-WhatIf</span></span>
<span data-ttu-id="fb3d9-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3d9-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3d9-134">CommonParameters</span></span>
<span data-ttu-id="fb3d9-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3d9-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3d9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fb3d9-137">INPUTS</span></span>

### <span data-ttu-id="fb3d9-138">System.object</span><span class="sxs-lookup"><span data-stu-id="fb3d9-138">System.String</span></span>

### <span data-ttu-id="fb3d9-139">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fb3d9-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="fb3d9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fb3d9-140">OUTPUTS</span></span>

### <span data-ttu-id="fb3d9-141">System.object</span><span class="sxs-lookup"><span data-stu-id="fb3d9-141">System.Boolean</span></span>

## <span data-ttu-id="fb3d9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="fb3d9-142">NOTES</span></span>

## <span data-ttu-id="fb3d9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb3d9-143">RELATED LINKS</span></span>
