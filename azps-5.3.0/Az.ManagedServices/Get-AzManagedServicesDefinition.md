---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439208"
---
# <span data-ttu-id="1fa75-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="1fa75-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="1fa75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fa75-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa75-103">取得特定的註冊定義或註冊定義的清單。</span><span class="sxs-lookup"><span data-stu-id="1fa75-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="1fa75-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fa75-104">SYNTAX</span></span>

### <span data-ttu-id="1fa75-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="1fa75-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fa75-106">設置</span><span class="sxs-lookup"><span data-stu-id="1fa75-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fa75-107">說明</span><span class="sxs-lookup"><span data-stu-id="1fa75-107">DESCRIPTION</span></span>
<span data-ttu-id="1fa75-108">取得特定的註冊定義或註冊定義的清單。</span><span class="sxs-lookup"><span data-stu-id="1fa75-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="1fa75-109">示例</span><span class="sxs-lookup"><span data-stu-id="1fa75-109">EXAMPLES</span></span>

### <span data-ttu-id="1fa75-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1fa75-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1fa75-111">取得預設作用中的所有註冊定義。</span><span class="sxs-lookup"><span data-stu-id="1fa75-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="1fa75-112">範例2</span><span class="sxs-lookup"><span data-stu-id="1fa75-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1fa75-113">在預設範圍內，以名稱取得註冊定義。</span><span class="sxs-lookup"><span data-stu-id="1fa75-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="1fa75-114">範例3</span><span class="sxs-lookup"><span data-stu-id="1fa75-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="1fa75-115">取得指定範圍內的所有註冊定義。</span><span class="sxs-lookup"><span data-stu-id="1fa75-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="1fa75-116">參數</span><span class="sxs-lookup"><span data-stu-id="1fa75-116">PARAMETERS</span></span>

### <span data-ttu-id="1fa75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa75-117">-DefaultProfile</span></span>
<span data-ttu-id="1fa75-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fa75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fa75-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1fa75-119">-Name</span></span>
<span data-ttu-id="1fa75-120">註冊定義的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="1fa75-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="1fa75-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="1fa75-121">-Scope</span></span>
<span data-ttu-id="1fa75-122">已建立註冊定義的範圍。</span><span class="sxs-lookup"><span data-stu-id="1fa75-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="1fa75-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa75-123">CommonParameters</span></span>
<span data-ttu-id="1fa75-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fa75-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa75-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fa75-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa75-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1fa75-126">INPUTS</span></span>

### <span data-ttu-id="1fa75-127">所有</span><span class="sxs-lookup"><span data-stu-id="1fa75-127">None</span></span>
## <span data-ttu-id="1fa75-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1fa75-128">OUTPUTS</span></span>

### <span data-ttu-id="1fa75-129">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="1fa75-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="1fa75-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1fa75-130">NOTES</span></span>

## <span data-ttu-id="1fa75-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fa75-131">RELATED LINKS</span></span>
