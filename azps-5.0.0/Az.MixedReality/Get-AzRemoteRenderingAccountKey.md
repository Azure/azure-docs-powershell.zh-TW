---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138759"
---
# <span data-ttu-id="fde18-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="fde18-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="fde18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fde18-102">SYNOPSIS</span></span>
<span data-ttu-id="fde18-103">取得遠端轉譯帳戶的金鑰</span><span class="sxs-lookup"><span data-stu-id="fde18-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="fde18-104">句法</span><span class="sxs-lookup"><span data-stu-id="fde18-104">SYNTAX</span></span>

### <span data-ttu-id="fde18-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fde18-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fde18-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fde18-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fde18-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="fde18-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fde18-108">說明</span><span class="sxs-lookup"><span data-stu-id="fde18-108">DESCRIPTION</span></span>
<span data-ttu-id="fde18-109">取得遠端轉譯帳戶的開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="fde18-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="fde18-110">示例</span><span class="sxs-lookup"><span data-stu-id="fde18-110">EXAMPLES</span></span>

### <span data-ttu-id="fde18-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fde18-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="fde18-112">從目前的訂閱和資源群組 "rg1" 取得遠端轉譯帳戶「範例」的開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="fde18-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="fde18-113">範例2</span><span class="sxs-lookup"><span data-stu-id="fde18-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="fde18-114">從目前的訂閱和含有管道的資源群組 "rg1"，取得遠端轉譯帳戶 "範例" 的開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="fde18-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="fde18-115">參數</span><span class="sxs-lookup"><span data-stu-id="fde18-115">PARAMETERS</span></span>

### <span data-ttu-id="fde18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde18-116">-DefaultProfile</span></span>
<span data-ttu-id="fde18-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fde18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fde18-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fde18-118">-InputObject</span></span>
<span data-ttu-id="fde18-119">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="fde18-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fde18-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="fde18-120">-Name</span></span>
<span data-ttu-id="fde18-121">遠端轉譯帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fde18-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde18-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde18-122">-ResourceGroupName</span></span>
<span data-ttu-id="fde18-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fde18-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde18-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fde18-124">-ResourceId</span></span>
<span data-ttu-id="fde18-125">遠端轉譯帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fde18-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="fde18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde18-126">CommonParameters</span></span>
<span data-ttu-id="fde18-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fde18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fde18-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fde18-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde18-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fde18-129">INPUTS</span></span>

### <span data-ttu-id="fde18-130">System.object</span><span class="sxs-lookup"><span data-stu-id="fde18-130">System.String</span></span>

### <span data-ttu-id="fde18-131">MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="fde18-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="fde18-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fde18-132">OUTPUTS</span></span>

### <span data-ttu-id="fde18-133">MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fde18-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="fde18-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fde18-134">NOTES</span></span>

## <span data-ttu-id="fde18-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fde18-135">RELATED LINKS</span></span>
