---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/remove-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
ms.openlocfilehash: 9880bf574aec57796d185742b2f33b79da8f7c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446976"
---
# <span data-ttu-id="1bd4f-101">Remove-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="1bd4f-101">Remove-AzureRmMapsAccount</span></span>

## <span data-ttu-id="1bd4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd4f-103">刪除 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-103">Deletes an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bd4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bd4f-104">SYNTAX</span></span>

### <span data-ttu-id="1bd4f-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1bd4f-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd4f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bd4f-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd4f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bd4f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bd4f-108">說明</span><span class="sxs-lookup"><span data-stu-id="1bd4f-108">DESCRIPTION</span></span>
<span data-ttu-id="1bd4f-109">Remove-AzureRmMapsAccount Cmdlet 會刪除指定的 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-109">The Remove-AzureRmMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="1bd4f-110">示例</span><span class="sxs-lookup"><span data-stu-id="1bd4f-110">EXAMPLES</span></span>

### <span data-ttu-id="1bd4f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1bd4f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="1bd4f-112">從 [資源群組] MyResourceGroup 刪除帳戶我的帳戶。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="1bd4f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1bd4f-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="1bd4f-114">刪除指定的 Azure 地圖帳戶。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="1bd4f-115">參數</span><span class="sxs-lookup"><span data-stu-id="1bd4f-115">PARAMETERS</span></span>

### <span data-ttu-id="1bd4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd4f-116">-DefaultProfile</span></span>
<span data-ttu-id="1bd4f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bd4f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bd4f-118">-InputObject</span></span>
<span data-ttu-id="1bd4f-119">從 AzureRmMapsAccount 將 [地圖] 帳戶成管道。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="1bd4f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1bd4f-120">-Name</span></span>
<span data-ttu-id="1bd4f-121">地圖帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="1bd4f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bd4f-122">-PassThru</span></span>
<span data-ttu-id="1bd4f-123">返回是否已成功刪除指定的帳號。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="1bd4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="1bd4f-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1bd4f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bd4f-126">-ResourceId</span></span>
<span data-ttu-id="1bd4f-127">地圖帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="1bd4f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1bd4f-128">-Confirm</span></span>
<span data-ttu-id="1bd4f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bd4f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bd4f-130">-WhatIf</span></span>
<span data-ttu-id="1bd4f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bd4f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bd4f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd4f-133">CommonParameters</span></span>
<span data-ttu-id="1bd4f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd4f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bd4f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd4f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1bd4f-136">INPUTS</span></span>

### <span data-ttu-id="1bd4f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="1bd4f-137">System.String</span></span>

### <span data-ttu-id="1bd4f-138">PSMapsAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1bd4f-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="1bd4f-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1bd4f-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1bd4f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1bd4f-140">OUTPUTS</span></span>

### <span data-ttu-id="1bd4f-141">System.object</span><span class="sxs-lookup"><span data-stu-id="1bd4f-141">System.Boolean</span></span>

## <span data-ttu-id="1bd4f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1bd4f-142">NOTES</span></span>

## <span data-ttu-id="1bd4f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bd4f-143">RELATED LINKS</span></span>
