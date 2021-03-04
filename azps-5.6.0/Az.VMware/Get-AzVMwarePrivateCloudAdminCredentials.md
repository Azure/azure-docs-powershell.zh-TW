---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 88ecb5baff31ddcc27ce090f19a868c4d393c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910814"
---
# <span data-ttu-id="49343-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="49343-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="49343-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49343-102">SYNOPSIS</span></span>
<span data-ttu-id="49343-103">列出專用雲端的系統管理員認證</span><span class="sxs-lookup"><span data-stu-id="49343-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="49343-104">語法</span><span class="sxs-lookup"><span data-stu-id="49343-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49343-105">描述</span><span class="sxs-lookup"><span data-stu-id="49343-105">DESCRIPTION</span></span>
<span data-ttu-id="49343-106">列出專用雲端的系統管理員認證</span><span class="sxs-lookup"><span data-stu-id="49343-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="49343-107">例子</span><span class="sxs-lookup"><span data-stu-id="49343-107">EXAMPLES</span></span>

### <span data-ttu-id="49343-108">範例 1：取得專用雲端的系統管理員認證</span><span class="sxs-lookup"><span data-stu-id="49343-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="49343-109">取得私人雲端的系統管理員認證</span><span class="sxs-lookup"><span data-stu-id="49343-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="49343-110">參數</span><span class="sxs-lookup"><span data-stu-id="49343-110">PARAMETERS</span></span>

### <span data-ttu-id="49343-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49343-111">-DefaultProfile</span></span>
<span data-ttu-id="49343-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49343-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49343-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="49343-113">-PrivateCloudName</span></span>
<span data-ttu-id="49343-114">私人雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="49343-114">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49343-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49343-115">-ResourceGroupName</span></span>
<span data-ttu-id="49343-116">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49343-116">The name of the resource group.</span></span>
<span data-ttu-id="49343-117">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="49343-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49343-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49343-118">-SubscriptionId</span></span>
<span data-ttu-id="49343-119">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="49343-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49343-120">-確認</span><span class="sxs-lookup"><span data-stu-id="49343-120">-Confirm</span></span>
<span data-ttu-id="49343-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49343-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49343-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49343-122">-WhatIf</span></span>
<span data-ttu-id="49343-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49343-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49343-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49343-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49343-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49343-125">CommonParameters</span></span>
<span data-ttu-id="49343-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49343-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49343-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49343-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49343-128">輸入</span><span class="sxs-lookup"><span data-stu-id="49343-128">INPUTS</span></span>

## <span data-ttu-id="49343-129">輸出</span><span class="sxs-lookup"><span data-stu-id="49343-129">OUTPUTS</span></span>

### <span data-ttu-id="49343-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="49343-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="49343-131">筆記</span><span class="sxs-lookup"><span data-stu-id="49343-131">NOTES</span></span>

<span data-ttu-id="49343-132">別名</span><span class="sxs-lookup"><span data-stu-id="49343-132">ALIASES</span></span>

## <span data-ttu-id="49343-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="49343-133">RELATED LINKS</span></span>

