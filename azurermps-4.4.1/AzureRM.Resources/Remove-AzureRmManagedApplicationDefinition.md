---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454864"
---
# <span data-ttu-id="d45ff-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="d45ff-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="d45ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d45ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d45ff-103">移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="d45ff-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d45ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="d45ff-104">SYNTAX</span></span>

### <span data-ttu-id="d45ff-105">已設定受管理的應用程式定義名稱參數。</span><span class="sxs-lookup"><span data-stu-id="d45ff-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="d45ff-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="d45ff-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d45ff-107">已設定受管理的應用程式定義識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="d45ff-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d45ff-108">說明</span><span class="sxs-lookup"><span data-stu-id="d45ff-108">DESCRIPTION</span></span>
<span data-ttu-id="d45ff-109">**AzureRmManagedApplicationDefinition** Cmdlet 會移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="d45ff-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="d45ff-110">示例</span><span class="sxs-lookup"><span data-stu-id="d45ff-110">EXAMPLES</span></span>

### <span data-ttu-id="d45ff-111">範例1：以資源識別碼移除受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="d45ff-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="d45ff-112">第一個命令會使用 Get-AzureRmManagedApplicationDefinition Cmdlet 來取得名為 myAppDef 的管理應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="d45ff-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="d45ff-113">該命令會將它儲存在 $ApplicationDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="d45ff-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="d45ff-114">第二個命令會移除由 $ApplicationDefinition 的 **ResourceId** 屬性所識別的受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="d45ff-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="d45ff-115">參數</span><span class="sxs-lookup"><span data-stu-id="d45ff-115">PARAMETERS</span></span>

### <span data-ttu-id="d45ff-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d45ff-116">-ApiVersion</span></span>
<span data-ttu-id="d45ff-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d45ff-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d45ff-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="d45ff-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45ff-119">-DefaultProfile</span></span>
<span data-ttu-id="d45ff-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d45ff-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d45ff-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d45ff-121">-Force</span></span>
<span data-ttu-id="d45ff-122">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="d45ff-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d45ff-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d45ff-123">-Id</span></span>
<span data-ttu-id="d45ff-124">完全限定的管理應用程式定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="d45ff-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="d45ff-125">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d45ff-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d45ff-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d45ff-126">-Name</span></span>
<span data-ttu-id="d45ff-127">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="d45ff-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d45ff-128">-預先</span><span class="sxs-lookup"><span data-stu-id="d45ff-128">-Pre</span></span>
<span data-ttu-id="d45ff-129">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="d45ff-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d45ff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d45ff-130">-ResourceGroupName</span></span>
<span data-ttu-id="d45ff-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d45ff-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d45ff-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d45ff-132">-Confirm</span></span>
<span data-ttu-id="d45ff-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d45ff-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45ff-134">-WhatIf</span></span>
<span data-ttu-id="d45ff-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d45ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d45ff-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d45ff-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45ff-137">CommonParameters</span></span>
<span data-ttu-id="d45ff-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d45ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45ff-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d45ff-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45ff-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d45ff-140">INPUTS</span></span>

### <span data-ttu-id="d45ff-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d45ff-141">System.String</span></span>

## <span data-ttu-id="d45ff-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d45ff-142">OUTPUTS</span></span>

### <span data-ttu-id="d45ff-143">System.object</span><span class="sxs-lookup"><span data-stu-id="d45ff-143">System.Boolean</span></span>

## <span data-ttu-id="d45ff-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d45ff-144">NOTES</span></span>

## <span data-ttu-id="d45ff-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d45ff-145">RELATED LINKS</span></span>

