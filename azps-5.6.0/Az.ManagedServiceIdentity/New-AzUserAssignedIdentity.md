---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1c4395c4e2c36fd07fee6345c1a5ff7d724b7c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907858"
---
# <span data-ttu-id="cadf0-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cadf0-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="cadf0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cadf0-102">SYNOPSIS</span></span>
<span data-ttu-id="cadf0-103">建立新的使用者指派身分識別，或更新現有的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="cadf0-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="cadf0-104">語法</span><span class="sxs-lookup"><span data-stu-id="cadf0-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cadf0-105">描述</span><span class="sxs-lookup"><span data-stu-id="cadf0-105">DESCRIPTION</span></span>
<span data-ttu-id="cadf0-106">**New-AzUserAssignedIdentity Cmdlet** 會建立新的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="cadf0-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="cadf0-107">當與現有的身分識別一起使用時，它會更新身分識別。</span><span class="sxs-lookup"><span data-stu-id="cadf0-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="cadf0-108">若要新增 Azure Resource Manager 標籤至身分識別，請使用 Set-AzResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cadf0-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="cadf0-109">例子</span><span class="sxs-lookup"><span data-stu-id="cadf0-109">EXAMPLES</span></span>

### <span data-ttu-id="cadf0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="cadf0-110">Example 1</span></span>
<span data-ttu-id="cadf0-111">此範例 Cmdlet 在 ResourceGroup 位置的資源群組 **PSRG** 下，會使用名稱 **ID1** 建立一個新的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="cadf0-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="cadf0-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="cadf0-112">Example 2</span></span>
<span data-ttu-id="cadf0-113">此範例 Cmdlet 會以名稱 **ID1** 在西部地區資源群組 **PSRG** 下建立一個新的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="cadf0-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="cadf0-114">參數</span><span class="sxs-lookup"><span data-stu-id="cadf0-114">PARAMETERS</span></span>

### <span data-ttu-id="cadf0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cadf0-115">-AsJob</span></span>
<span data-ttu-id="cadf0-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cadf0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cadf0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadf0-117">-DefaultProfile</span></span>
<span data-ttu-id="cadf0-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cadf0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cadf0-119">-位置</span><span class="sxs-lookup"><span data-stu-id="cadf0-119">-Location</span></span>
<span data-ttu-id="cadf0-120">應建立身分識別的 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="cadf0-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadf0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cadf0-121">-Name</span></span>
<span data-ttu-id="cadf0-122">身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="cadf0-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadf0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadf0-123">-ResourceGroupName</span></span>
<span data-ttu-id="cadf0-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cadf0-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadf0-125">-標記</span><span class="sxs-lookup"><span data-stu-id="cadf0-125">-Tag</span></span>
<span data-ttu-id="cadf0-126">與身分識別相關聯的 Azure Resource Manager 標記。</span><span class="sxs-lookup"><span data-stu-id="cadf0-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadf0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="cadf0-127">-Confirm</span></span>
<span data-ttu-id="cadf0-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cadf0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cadf0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cadf0-129">-WhatIf</span></span>
<span data-ttu-id="cadf0-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cadf0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cadf0-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cadf0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cadf0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadf0-132">CommonParameters</span></span>
<span data-ttu-id="cadf0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cadf0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadf0-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cadf0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadf0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="cadf0-135">INPUTS</span></span>

### <span data-ttu-id="cadf0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cadf0-136">System.String</span></span>

### <span data-ttu-id="cadf0-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cadf0-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cadf0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="cadf0-138">OUTPUTS</span></span>

### <span data-ttu-id="cadf0-139">Microsoft.Azure.Commands.ManagedServiceIdentity.models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cadf0-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="cadf0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="cadf0-140">NOTES</span></span>

## <span data-ttu-id="cadf0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="cadf0-141">RELATED LINKS</span></span>
