---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
ms.openlocfilehash: 04f914dfd54d645f3c0ae7621cafaf20099f05c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916615"
---
# <span data-ttu-id="bdb9c-101">Get-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="bdb9c-101">Get-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="bdb9c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bdb9c-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb9c-103">取得遠端呈現帳戶</span><span class="sxs-lookup"><span data-stu-id="bdb9c-103">Get Remote Rendering Account</span></span>

## <span data-ttu-id="bdb9c-104">語法</span><span class="sxs-lookup"><span data-stu-id="bdb9c-104">SYNTAX</span></span>

### <span data-ttu-id="bdb9c-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bdb9c-105">ListParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb9c-106">GetParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bdb9c-106">GetParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb9c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb9c-107">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdb9c-108">描述</span><span class="sxs-lookup"><span data-stu-id="bdb9c-108">DESCRIPTION</span></span>
<span data-ttu-id="bdb9c-109">取得或列出特定訂閱 (資源) 的遠端呈現帳戶。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-109">Get or list Remote Rendering Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="bdb9c-110">例子</span><span class="sxs-lookup"><span data-stu-id="bdb9c-110">EXAMPLES</span></span>

### <span data-ttu-id="bdb9c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="bdb9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="bdb9c-112">在資源群組 "rg1" 中列出所有遠端呈現帳戶。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-112">List all Remote Rendering Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="bdb9c-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="bdb9c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="bdb9c-114">在資源群組 "rg1" 中取得遠端呈現帳戶的「範例」。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-114">Get Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="bdb9c-115">參數</span><span class="sxs-lookup"><span data-stu-id="bdb9c-115">PARAMETERS</span></span>

### <span data-ttu-id="bdb9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb9c-116">-DefaultProfile</span></span>
<span data-ttu-id="bdb9c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb9c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdb9c-118">-Name</span></span>
<span data-ttu-id="bdb9c-119">遠端呈現帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-119">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb9c-120">-ResourceGroupName</span></span>
<span data-ttu-id="bdb9c-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb9c-122">-ResourceId</span></span>
<span data-ttu-id="bdb9c-123">遠端呈現帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-123">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb9c-124">CommonParameters</span></span>
<span data-ttu-id="bdb9c-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bdb9c-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bdb9c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb9c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bdb9c-127">INPUTS</span></span>

### <span data-ttu-id="bdb9c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bdb9c-128">System.String</span></span>

## <span data-ttu-id="bdb9c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bdb9c-129">OUTPUTS</span></span>

### <span data-ttu-id="bdb9c-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="bdb9c-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="bdb9c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bdb9c-131">NOTES</span></span>

## <span data-ttu-id="bdb9c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdb9c-132">RELATED LINKS</span></span>
