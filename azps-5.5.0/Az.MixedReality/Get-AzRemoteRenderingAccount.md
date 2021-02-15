---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
ms.openlocfilehash: 9d4faa4a51352902330286722a005fae1b42bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136066"
---
# <span data-ttu-id="1af97-101">Get-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="1af97-101">Get-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="1af97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1af97-102">SYNOPSIS</span></span>
<span data-ttu-id="1af97-103">取得遠端轉譯帳戶</span><span class="sxs-lookup"><span data-stu-id="1af97-103">Get Remote Rendering Account</span></span>

## <span data-ttu-id="1af97-104">句法</span><span class="sxs-lookup"><span data-stu-id="1af97-104">SYNTAX</span></span>

### <span data-ttu-id="1af97-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1af97-105">ListParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af97-106">GetParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1af97-106">GetParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af97-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af97-107">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af97-108">說明</span><span class="sxs-lookup"><span data-stu-id="1af97-108">DESCRIPTION</span></span>
<span data-ttu-id="1af97-109">在特定的訂閱和資源群組中取得或列出遠端轉譯帳戶 (s) 。</span><span class="sxs-lookup"><span data-stu-id="1af97-109">Get or list Remote Rendering Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="1af97-110">示例</span><span class="sxs-lookup"><span data-stu-id="1af97-110">EXAMPLES</span></span>

### <span data-ttu-id="1af97-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1af97-111">Example 1</span></span>
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

<span data-ttu-id="1af97-112">列出 [資源] 群組中的所有遠端轉譯帳戶 [rg1]。</span><span class="sxs-lookup"><span data-stu-id="1af97-112">List all Remote Rendering Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="1af97-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1af97-113">Example 2</span></span>
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

<span data-ttu-id="1af97-114">取得資源群組 "rg1" 中的遠端轉譯帳戶「範例」。</span><span class="sxs-lookup"><span data-stu-id="1af97-114">Get Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="1af97-115">參數</span><span class="sxs-lookup"><span data-stu-id="1af97-115">PARAMETERS</span></span>

### <span data-ttu-id="1af97-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af97-116">-DefaultProfile</span></span>
<span data-ttu-id="1af97-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1af97-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af97-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1af97-118">-Name</span></span>
<span data-ttu-id="1af97-119">遠端轉譯帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1af97-119">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="1af97-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af97-120">-ResourceGroupName</span></span>
<span data-ttu-id="1af97-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1af97-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="1af97-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af97-122">-ResourceId</span></span>
<span data-ttu-id="1af97-123">遠端轉譯帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1af97-123">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="1af97-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af97-124">CommonParameters</span></span>
<span data-ttu-id="1af97-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1af97-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1af97-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1af97-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af97-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1af97-127">INPUTS</span></span>

### <span data-ttu-id="1af97-128">System.object</span><span class="sxs-lookup"><span data-stu-id="1af97-128">System.String</span></span>

## <span data-ttu-id="1af97-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1af97-129">OUTPUTS</span></span>

### <span data-ttu-id="1af97-130">MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="1af97-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="1af97-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1af97-131">NOTES</span></span>

## <span data-ttu-id="1af97-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1af97-132">RELATED LINKS</span></span>
