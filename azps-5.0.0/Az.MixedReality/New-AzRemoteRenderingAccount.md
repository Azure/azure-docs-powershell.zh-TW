---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138757"
---
# <span data-ttu-id="793c4-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="793c4-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="793c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="793c4-102">SYNOPSIS</span></span>
<span data-ttu-id="793c4-103">建立遠端轉譯帳戶</span><span class="sxs-lookup"><span data-stu-id="793c4-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="793c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="793c4-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="793c4-105">說明</span><span class="sxs-lookup"><span data-stu-id="793c4-105">DESCRIPTION</span></span>
<span data-ttu-id="793c4-106">在特定的訂閱、資源群組和區域中建立新的遠端轉譯帳戶。</span><span class="sxs-lookup"><span data-stu-id="793c4-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="793c4-107">示例</span><span class="sxs-lookup"><span data-stu-id="793c4-107">EXAMPLES</span></span>

### <span data-ttu-id="793c4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="793c4-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="793c4-109">在目前的訂閱中建立新的遠端轉譯帳戶 "範例"，資源群組 "rg1" 和美國中部。</span><span class="sxs-lookup"><span data-stu-id="793c4-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="793c4-110">參數</span><span class="sxs-lookup"><span data-stu-id="793c4-110">PARAMETERS</span></span>

### <span data-ttu-id="793c4-111">-確認</span><span class="sxs-lookup"><span data-stu-id="793c4-111">-Confirm</span></span>
<span data-ttu-id="793c4-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="793c4-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="793c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793c4-113">-DefaultProfile</span></span>
<span data-ttu-id="793c4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="793c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="793c4-115">-位置</span><span class="sxs-lookup"><span data-stu-id="793c4-115">-Location</span></span>
<span data-ttu-id="793c4-116">遠端轉譯帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="793c4-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793c4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="793c4-117">-Name</span></span>
<span data-ttu-id="793c4-118">遠端轉譯帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="793c4-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="793c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="793c4-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="793c4-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="793c4-121">-WhatIf</span></span>
<span data-ttu-id="793c4-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="793c4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="793c4-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="793c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="793c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793c4-124">CommonParameters</span></span>
<span data-ttu-id="793c4-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="793c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="793c4-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="793c4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793c4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="793c4-127">INPUTS</span></span>

### <span data-ttu-id="793c4-128">所有</span><span class="sxs-lookup"><span data-stu-id="793c4-128">None</span></span>

## <span data-ttu-id="793c4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="793c4-129">OUTPUTS</span></span>

### <span data-ttu-id="793c4-130">MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="793c4-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="793c4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="793c4-131">NOTES</span></span>

## <span data-ttu-id="793c4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="793c4-132">RELATED LINKS</span></span>
