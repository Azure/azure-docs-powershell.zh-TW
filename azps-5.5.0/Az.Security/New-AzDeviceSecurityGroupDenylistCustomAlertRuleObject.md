---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142560"
---
# <span data-ttu-id="6dea6-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="6dea6-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="6dea6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6dea6-102">SYNOPSIS</span></span>
<span data-ttu-id="6dea6-103">為裝置安全性群組建立新的 [拒絕清單] 自訂警示規則 (IoT 安全性) </span><span class="sxs-lookup"><span data-stu-id="6dea6-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="6dea6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6dea6-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dea6-105">說明</span><span class="sxs-lookup"><span data-stu-id="6dea6-105">DESCRIPTION</span></span>
<span data-ttu-id="6dea6-106">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject Cmdlet 會在 IoT security 方案中為 device security 群組建立新的 denyed 自訂警報規則清單。</span><span class="sxs-lookup"><span data-stu-id="6dea6-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="6dea6-107">示例</span><span class="sxs-lookup"><span data-stu-id="6dea6-107">EXAMPLES</span></span>

### <span data-ttu-id="6dea6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6dea6-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="6dea6-109">建立新的 [拒絕清單] 自訂警示規則，並將 [rull 類型] 設定為 [desable]</span><span class="sxs-lookup"><span data-stu-id="6dea6-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="6dea6-110">參數</span><span class="sxs-lookup"><span data-stu-id="6dea6-110">PARAMETERS</span></span>

### <span data-ttu-id="6dea6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dea6-111">-DefaultProfile</span></span>
<span data-ttu-id="6dea6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6dea6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dea6-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="6dea6-113">-DenylistValue</span></span>
<span data-ttu-id="6dea6-114">[拒絕] 清單值。</span><span class="sxs-lookup"><span data-stu-id="6dea6-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dea6-115">-啟用</span><span class="sxs-lookup"><span data-stu-id="6dea6-115">-Enabled</span></span>
<span data-ttu-id="6dea6-116">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="6dea6-116">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dea6-117">-類型</span><span class="sxs-lookup"><span data-stu-id="6dea6-117">-Type</span></span>
<span data-ttu-id="6dea6-118">規則類型。</span><span class="sxs-lookup"><span data-stu-id="6dea6-118">Rule type.</span></span>

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

### <span data-ttu-id="6dea6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dea6-119">CommonParameters</span></span>
<span data-ttu-id="6dea6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6dea6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dea6-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6dea6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dea6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="6dea6-122">INPUTS</span></span>

### <span data-ttu-id="6dea6-123">所有</span><span class="sxs-lookup"><span data-stu-id="6dea6-123">None</span></span>

## <span data-ttu-id="6dea6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6dea6-124">OUTPUTS</span></span>

### <span data-ttu-id="6dea6-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="6dea6-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="6dea6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="6dea6-126">NOTES</span></span>

## <span data-ttu-id="6dea6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="6dea6-127">RELATED LINKS</span></span>
