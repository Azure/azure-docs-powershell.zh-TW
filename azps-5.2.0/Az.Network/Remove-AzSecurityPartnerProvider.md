---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281255"
---
# <span data-ttu-id="d689e-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d689e-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="d689e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d689e-102">SYNOPSIS</span></span>
<span data-ttu-id="d689e-103">刪除 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="d689e-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="d689e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d689e-104">SYNTAX</span></span>

### <span data-ttu-id="d689e-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d689e-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d689e-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d689e-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d689e-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d689e-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d689e-108">說明</span><span class="sxs-lookup"><span data-stu-id="d689e-108">DESCRIPTION</span></span>
<span data-ttu-id="d689e-109">**AzSecurityPartnerProvider** Cmdlet 會刪除 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d689e-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="d689e-110">示例</span><span class="sxs-lookup"><span data-stu-id="d689e-110">EXAMPLES</span></span>

### <span data-ttu-id="d689e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d689e-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="d689e-112">參數</span><span class="sxs-lookup"><span data-stu-id="d689e-112">PARAMETERS</span></span>

### <span data-ttu-id="d689e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d689e-113">-AsJob</span></span>
<span data-ttu-id="d689e-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d689e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d689e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d689e-115">-DefaultProfile</span></span>
<span data-ttu-id="d689e-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d689e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d689e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d689e-117">-Force</span></span>
<span data-ttu-id="d689e-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d689e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d689e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d689e-119">-Name</span></span>
<span data-ttu-id="d689e-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d689e-120">The resource name.</span></span>

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

### <span data-ttu-id="d689e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d689e-121">-PassThru</span></span>
<span data-ttu-id="d689e-122">傳回代表執行此作業之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d689e-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="d689e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d689e-123">-ResourceGroupName</span></span>
<span data-ttu-id="d689e-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d689e-124">The resource group name.</span></span>

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

### <span data-ttu-id="d689e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d689e-125">-ResourceId</span></span>
<span data-ttu-id="d689e-126">SecurityPartnerProvider 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d689e-126">The securityPartnerProvider resource Id.</span></span>

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

### <span data-ttu-id="d689e-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d689e-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="d689e-128">SecurityPartnerProvider 輸入物件。</span><span class="sxs-lookup"><span data-stu-id="d689e-128">The securityPartnerProvider input object.</span></span>

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

### <span data-ttu-id="d689e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d689e-129">-Confirm</span></span>
<span data-ttu-id="d689e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d689e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d689e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d689e-131">-WhatIf</span></span>
<span data-ttu-id="d689e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d689e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d689e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d689e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d689e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d689e-134">CommonParameters</span></span>
<span data-ttu-id="d689e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d689e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d689e-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d689e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d689e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d689e-137">INPUTS</span></span>

### <span data-ttu-id="d689e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d689e-138">System.String</span></span>

### <span data-ttu-id="d689e-139">PSSecurityPartnerProvider 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d689e-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="d689e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d689e-140">OUTPUTS</span></span>

### <span data-ttu-id="d689e-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d689e-141">System.Boolean</span></span>

## <span data-ttu-id="d689e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d689e-142">NOTES</span></span>

## <span data-ttu-id="d689e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d689e-143">RELATED LINKS</span></span>
