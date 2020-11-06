---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452224"
---
# <span data-ttu-id="579b0-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="579b0-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="579b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="579b0-102">SYNOPSIS</span></span>
<span data-ttu-id="579b0-103">刪除 [以位置為基礎的服務帳戶]。</span><span class="sxs-lookup"><span data-stu-id="579b0-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="579b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="579b0-104">SYNTAX</span></span>

### <span data-ttu-id="579b0-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="579b0-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="579b0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="579b0-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="579b0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="579b0-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="579b0-108">說明</span><span class="sxs-lookup"><span data-stu-id="579b0-108">DESCRIPTION</span></span>
<span data-ttu-id="579b0-109">**AzureRmLocationBasedServicesAccount** Cmdlet 會刪除指定的 [以位置為基礎的服務帳戶]。</span><span class="sxs-lookup"><span data-stu-id="579b0-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="579b0-110">示例</span><span class="sxs-lookup"><span data-stu-id="579b0-110">EXAMPLES</span></span>

### <span data-ttu-id="579b0-111">範例1</span><span class="sxs-lookup"><span data-stu-id="579b0-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="579b0-112">從 [資源群組] MyResourceGroup 刪除帳戶我的帳戶。</span><span class="sxs-lookup"><span data-stu-id="579b0-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="579b0-113">範例2</span><span class="sxs-lookup"><span data-stu-id="579b0-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="579b0-114">刪除指定的 [以位置為基礎的服務帳戶]。</span><span class="sxs-lookup"><span data-stu-id="579b0-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="579b0-115">參數</span><span class="sxs-lookup"><span data-stu-id="579b0-115">PARAMETERS</span></span>

### <span data-ttu-id="579b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579b0-116">-DefaultProfile</span></span>
<span data-ttu-id="579b0-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="579b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="579b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="579b0-118">-InputObject</span></span>
<span data-ttu-id="579b0-119">[以位置為基礎的服務] 帳戶從 [AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md)中進行管道。</span><span class="sxs-lookup"><span data-stu-id="579b0-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="579b0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="579b0-120">-Name</span></span>
<span data-ttu-id="579b0-121">[以位置為基礎的服務] 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="579b0-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="579b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="579b0-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="579b0-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579b0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="579b0-124">-ResourceId</span></span>
<span data-ttu-id="579b0-125">基於位置的服務帳戶 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="579b0-125">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579b0-126">-確認</span><span class="sxs-lookup"><span data-stu-id="579b0-126">-Confirm</span></span>
<span data-ttu-id="579b0-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="579b0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="579b0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="579b0-128">-WhatIf</span></span>
<span data-ttu-id="579b0-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="579b0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="579b0-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="579b0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="579b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579b0-131">CommonParameters</span></span>
<span data-ttu-id="579b0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="579b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579b0-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="579b0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579b0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="579b0-134">INPUTS</span></span>

### <span data-ttu-id="579b0-135">System.object</span><span class="sxs-lookup"><span data-stu-id="579b0-135">System.String</span></span>

## <span data-ttu-id="579b0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="579b0-136">OUTPUTS</span></span>

### <span data-ttu-id="579b0-137">System.object</span><span class="sxs-lookup"><span data-stu-id="579b0-137">System.Object</span></span>

## <span data-ttu-id="579b0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="579b0-138">NOTES</span></span>

## <span data-ttu-id="579b0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="579b0-139">RELATED LINKS</span></span>
