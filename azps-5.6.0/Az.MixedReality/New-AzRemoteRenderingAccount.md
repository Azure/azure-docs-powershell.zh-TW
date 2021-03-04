---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: df65bd7b8dfd2f3091590b8830059965e599c029
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907853"
---
# <span data-ttu-id="eacaf-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="eacaf-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="eacaf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eacaf-102">SYNOPSIS</span></span>
<span data-ttu-id="eacaf-103">建立遠端呈現帳戶</span><span class="sxs-lookup"><span data-stu-id="eacaf-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="eacaf-104">語法</span><span class="sxs-lookup"><span data-stu-id="eacaf-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eacaf-105">描述</span><span class="sxs-lookup"><span data-stu-id="eacaf-105">DESCRIPTION</span></span>
<span data-ttu-id="eacaf-106">在特定訂閱、資源群組和地區中建立新的遠端呈現帳戶。</span><span class="sxs-lookup"><span data-stu-id="eacaf-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="eacaf-107">例子</span><span class="sxs-lookup"><span data-stu-id="eacaf-107">EXAMPLES</span></span>

### <span data-ttu-id="eacaf-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="eacaf-108">Example 1</span></span>
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

<span data-ttu-id="eacaf-109">在目前的訂閱、資源群組 "rg1" 和美國中，建立新的遠端呈現帳戶"範例"。</span><span class="sxs-lookup"><span data-stu-id="eacaf-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="eacaf-110">參數</span><span class="sxs-lookup"><span data-stu-id="eacaf-110">PARAMETERS</span></span>

### <span data-ttu-id="eacaf-111">-確認</span><span class="sxs-lookup"><span data-stu-id="eacaf-111">-Confirm</span></span>
<span data-ttu-id="eacaf-112">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eacaf-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eacaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eacaf-113">-DefaultProfile</span></span>
<span data-ttu-id="eacaf-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eacaf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eacaf-115">-位置</span><span class="sxs-lookup"><span data-stu-id="eacaf-115">-Location</span></span>
<span data-ttu-id="eacaf-116">遠端呈現帳戶位置。</span><span class="sxs-lookup"><span data-stu-id="eacaf-116">Remote Rendering Account Location.</span></span>

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

### <span data-ttu-id="eacaf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="eacaf-117">-Name</span></span>
<span data-ttu-id="eacaf-118">遠端呈現帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="eacaf-118">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="eacaf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eacaf-119">-ResourceGroupName</span></span>
<span data-ttu-id="eacaf-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="eacaf-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="eacaf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eacaf-121">-WhatIf</span></span>
<span data-ttu-id="eacaf-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eacaf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eacaf-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eacaf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eacaf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eacaf-124">CommonParameters</span></span>
<span data-ttu-id="eacaf-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eacaf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eacaf-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eacaf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eacaf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="eacaf-127">INPUTS</span></span>

### <span data-ttu-id="eacaf-128">沒有</span><span class="sxs-lookup"><span data-stu-id="eacaf-128">None</span></span>

## <span data-ttu-id="eacaf-129">輸出</span><span class="sxs-lookup"><span data-stu-id="eacaf-129">OUTPUTS</span></span>

### <span data-ttu-id="eacaf-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="eacaf-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="eacaf-131">筆記</span><span class="sxs-lookup"><span data-stu-id="eacaf-131">NOTES</span></span>

## <span data-ttu-id="eacaf-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="eacaf-132">RELATED LINKS</span></span>
