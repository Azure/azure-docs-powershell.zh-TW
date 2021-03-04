---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 80c315b5bb2e1a1bcd15a2b9686a1201739171a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916735"
---
# <span data-ttu-id="d1334-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d1334-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="d1334-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1334-102">SYNOPSIS</span></span>
<span data-ttu-id="d1334-103">獲得特定的註冊定義或註冊定義清單。</span><span class="sxs-lookup"><span data-stu-id="d1334-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="d1334-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1334-104">SYNTAX</span></span>

### <span data-ttu-id="d1334-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d1334-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1334-106">預設</span><span class="sxs-lookup"><span data-stu-id="d1334-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1334-107">描述</span><span class="sxs-lookup"><span data-stu-id="d1334-107">DESCRIPTION</span></span>
<span data-ttu-id="d1334-108">獲得特定的註冊定義或註冊定義清單。</span><span class="sxs-lookup"><span data-stu-id="d1334-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="d1334-109">例子</span><span class="sxs-lookup"><span data-stu-id="d1334-109">EXAMPLES</span></span>

### <span data-ttu-id="d1334-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="d1334-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="d1334-111">在預設範圍中獲得所有註冊定義。</span><span class="sxs-lookup"><span data-stu-id="d1334-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="d1334-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="d1334-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="d1334-113">在預設範圍中按照名稱來獲得註冊定義。</span><span class="sxs-lookup"><span data-stu-id="d1334-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="d1334-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="d1334-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="d1334-115">在給定範圍中獲得所有註冊定義。</span><span class="sxs-lookup"><span data-stu-id="d1334-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="d1334-116">參數</span><span class="sxs-lookup"><span data-stu-id="d1334-116">PARAMETERS</span></span>

### <span data-ttu-id="d1334-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1334-117">-DefaultProfile</span></span>
<span data-ttu-id="d1334-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1334-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1334-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1334-119">-Name</span></span>
<span data-ttu-id="d1334-120">註冊定義的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d1334-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1334-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="d1334-121">-Scope</span></span>
<span data-ttu-id="d1334-122">建立註冊定義的範圍。</span><span class="sxs-lookup"><span data-stu-id="d1334-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="d1334-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1334-123">CommonParameters</span></span>
<span data-ttu-id="d1334-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1334-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1334-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1334-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1334-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d1334-126">INPUTS</span></span>

### <span data-ttu-id="d1334-127">沒有</span><span class="sxs-lookup"><span data-stu-id="d1334-127">None</span></span>
## <span data-ttu-id="d1334-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d1334-128">OUTPUTS</span></span>

### <span data-ttu-id="d1334-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="d1334-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="d1334-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d1334-130">NOTES</span></span>

## <span data-ttu-id="d1334-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1334-131">RELATED LINKS</span></span>
