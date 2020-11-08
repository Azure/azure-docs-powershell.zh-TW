---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128637"
---
# <span data-ttu-id="66918-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="66918-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="66918-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66918-102">SYNOPSIS</span></span>
<span data-ttu-id="66918-103">取得受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="66918-103">Gets managed application definitions</span></span>

## <span data-ttu-id="66918-104">句法</span><span class="sxs-lookup"><span data-stu-id="66918-104">SYNTAX</span></span>

### <span data-ttu-id="66918-105">GetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="66918-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66918-106">GetById</span><span class="sxs-lookup"><span data-stu-id="66918-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66918-107">說明</span><span class="sxs-lookup"><span data-stu-id="66918-107">DESCRIPTION</span></span>
<span data-ttu-id="66918-108">AzManagedApplicationDefinition Cmdlet 會取得受管理 **的** 應用程式定義</span><span class="sxs-lookup"><span data-stu-id="66918-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="66918-109">示例</span><span class="sxs-lookup"><span data-stu-id="66918-109">EXAMPLES</span></span>

### <span data-ttu-id="66918-110">範例1：取得資源群組下所有受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="66918-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="66918-111">這個命令會在 [資源群組] 的 [MyRG] 下取得受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="66918-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="66918-112">範例2：取得受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="66918-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="66918-113">這個命令會在資源群組 "MyRG" 下取得受管理的應用程式定義 "myManagedAppDef"</span><span class="sxs-lookup"><span data-stu-id="66918-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="66918-114">參數</span><span class="sxs-lookup"><span data-stu-id="66918-114">PARAMETERS</span></span>

### <span data-ttu-id="66918-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66918-115">-ApiVersion</span></span>
<span data-ttu-id="66918-116">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="66918-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="66918-117">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="66918-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="66918-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66918-118">-DefaultProfile</span></span>
<span data-ttu-id="66918-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66918-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66918-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="66918-120">-Id</span></span>
<span data-ttu-id="66918-121">完全限定的管理應用程式定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="66918-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="66918-122">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="66918-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66918-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="66918-123">-Name</span></span>
<span data-ttu-id="66918-124">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="66918-124">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66918-125">-預先</span><span class="sxs-lookup"><span data-stu-id="66918-125">-Pre</span></span>
<span data-ttu-id="66918-126">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="66918-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="66918-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66918-127">-ResourceGroupName</span></span>
<span data-ttu-id="66918-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66918-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66918-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66918-129">CommonParameters</span></span>
<span data-ttu-id="66918-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66918-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66918-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66918-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66918-132">輸入</span><span class="sxs-lookup"><span data-stu-id="66918-132">INPUTS</span></span>

### <span data-ttu-id="66918-133">System.object</span><span class="sxs-lookup"><span data-stu-id="66918-133">System.String</span></span>

## <span data-ttu-id="66918-134">輸出</span><span class="sxs-lookup"><span data-stu-id="66918-134">OUTPUTS</span></span>

### <span data-ttu-id="66918-135">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="66918-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="66918-136">筆記</span><span class="sxs-lookup"><span data-stu-id="66918-136">NOTES</span></span>

## <span data-ttu-id="66918-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="66918-137">RELATED LINKS</span></span>