---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 8b533f26b7fa947a185ee0be2dc5a395e77ebbbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449888"
---
# <span data-ttu-id="1c064-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1c064-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="1c064-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c064-102">SYNOPSIS</span></span>
<span data-ttu-id="1c064-103">移除指派身分識別的使用者。</span><span class="sxs-lookup"><span data-stu-id="1c064-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c064-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c064-104">SYNTAX</span></span>

### <span data-ttu-id="1c064-105">ResourceGroupAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1c064-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c064-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c064-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c064-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c064-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c064-108">說明</span><span class="sxs-lookup"><span data-stu-id="1c064-108">DESCRIPTION</span></span>
<span data-ttu-id="1c064-109">[ **移除-AzureRmUserAssignedIdentity** ] 會刪除指定的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="1c064-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="1c064-110">示例</span><span class="sxs-lookup"><span data-stu-id="1c064-110">EXAMPLES</span></span>

### <span data-ttu-id="1c064-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1c064-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="1c064-112">這個範例 Cmdlet 會刪除 [資源群組 **PSRG** ] 下的 [身分識別 **ID1** ]。</span><span class="sxs-lookup"><span data-stu-id="1c064-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>

<span data-ttu-id="1c064-113">滿足</span><span class="sxs-lookup"><span data-stu-id="1c064-113">True</span></span>

## <span data-ttu-id="1c064-114">參數</span><span class="sxs-lookup"><span data-stu-id="1c064-114">PARAMETERS</span></span>

### <span data-ttu-id="1c064-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c064-115">-AsJob</span></span>
<span data-ttu-id="1c064-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1c064-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c064-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c064-117">-DefaultProfile</span></span>
<span data-ttu-id="1c064-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c064-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c064-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1c064-119">-Force</span></span>
<span data-ttu-id="1c064-120">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="1c064-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="1c064-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c064-121">-InputObject</span></span>
<span data-ttu-id="1c064-122">身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="1c064-122">The Identity object.</span></span>

```yaml
Type: PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c064-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c064-123">-Name</span></span>
<span data-ttu-id="1c064-124">身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="1c064-124">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c064-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c064-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c064-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c064-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c064-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c064-127">-ResourceId</span></span>
<span data-ttu-id="1c064-128">身分識別的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c064-128">The Identity's resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c064-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1c064-129">-Confirm</span></span>
<span data-ttu-id="1c064-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1c064-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c064-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c064-131">-WhatIf</span></span>
<span data-ttu-id="1c064-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c064-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c064-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c064-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c064-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c064-134">CommonParameters</span></span>
<span data-ttu-id="1c064-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c064-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c064-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c064-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c064-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1c064-137">INPUTS</span></span>

### <span data-ttu-id="1c064-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1c064-138">System.String</span></span>

## <span data-ttu-id="1c064-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1c064-139">OUTPUTS</span></span>

### <span data-ttu-id="1c064-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1c064-140">System.Boolean</span></span>

## <span data-ttu-id="1c064-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1c064-141">NOTES</span></span>

## <span data-ttu-id="1c064-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c064-142">RELATED LINKS</span></span>
