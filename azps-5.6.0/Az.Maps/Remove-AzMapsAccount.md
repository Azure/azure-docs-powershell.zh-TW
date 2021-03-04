---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: e14e080ab04c3fc9cb191c240e3d71c00cc1c7f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916114"
---
# <span data-ttu-id="2a1fe-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2a1fe-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="2a1fe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2a1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2a1fe-103">刪除 Azure 地圖服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="2a1fe-104">語法</span><span class="sxs-lookup"><span data-stu-id="2a1fe-104">SYNTAX</span></span>

### <span data-ttu-id="2a1fe-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2a1fe-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a1fe-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a1fe-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a1fe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a1fe-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a1fe-108">描述</span><span class="sxs-lookup"><span data-stu-id="2a1fe-108">DESCRIPTION</span></span>
<span data-ttu-id="2a1fe-109">Cmdlet Remove-AzMapsAccount刪除指定的 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="2a1fe-110">例子</span><span class="sxs-lookup"><span data-stu-id="2a1fe-110">EXAMPLES</span></span>

### <span data-ttu-id="2a1fe-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2a1fe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2a1fe-112">從資源群組 MyResourceGroup 刪除帳戶 MyAccount。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="2a1fe-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="2a1fe-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2a1fe-114">刪除指定的 Azure 地圖服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="2a1fe-115">參數</span><span class="sxs-lookup"><span data-stu-id="2a1fe-115">PARAMETERS</span></span>

### <span data-ttu-id="2a1fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a1fe-116">-DefaultProfile</span></span>
<span data-ttu-id="2a1fe-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a1fe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a1fe-118">-InputObject</span></span>
<span data-ttu-id="2a1fe-119">從 Get-AzMapsAccount移來的地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1fe-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a1fe-120">-Name</span></span>
<span data-ttu-id="2a1fe-121">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1fe-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a1fe-122">-PassThru</span></span>
<span data-ttu-id="2a1fe-123">返回指定的帳號是否已成功刪除。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="2a1fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a1fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a1fe-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1fe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a1fe-126">-ResourceId</span></span>
<span data-ttu-id="2a1fe-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1fe-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2a1fe-128">-Confirm</span></span>
<span data-ttu-id="2a1fe-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a1fe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a1fe-130">-WhatIf</span></span>
<span data-ttu-id="2a1fe-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a1fe-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a1fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a1fe-133">CommonParameters</span></span>
<span data-ttu-id="2a1fe-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a1fe-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2a1fe-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a1fe-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2a1fe-136">INPUTS</span></span>

### <span data-ttu-id="2a1fe-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2a1fe-137">System.String</span></span>

### <span data-ttu-id="2a1fe-138">Microsoft.Azure.Commands.Maps.models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="2a1fe-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="2a1fe-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2a1fe-139">OUTPUTS</span></span>

### <span data-ttu-id="2a1fe-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a1fe-140">System.Boolean</span></span>

## <span data-ttu-id="2a1fe-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2a1fe-141">NOTES</span></span>

## <span data-ttu-id="2a1fe-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a1fe-142">RELATED LINKS</span></span>
