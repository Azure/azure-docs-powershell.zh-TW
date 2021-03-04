---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: 0f46a0f009085aa7ef7b66ac91d621338a7358b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908742"
---
# <span data-ttu-id="39d29-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="39d29-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="39d29-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39d29-102">SYNOPSIS</span></span>
<span data-ttu-id="39d29-103">為裝置安全性群組建立新允許清單自訂提醒規則 (IoT 安全性) </span><span class="sxs-lookup"><span data-stu-id="39d29-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="39d29-104">語法</span><span class="sxs-lookup"><span data-stu-id="39d29-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39d29-105">描述</span><span class="sxs-lookup"><span data-stu-id="39d29-105">DESCRIPTION</span></span>
<span data-ttu-id="39d29-106">Cmdlet New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject為 IoT 安全性解決方案中的裝置安全性群組建立允許的自訂通知規則新清單。</span><span class="sxs-lookup"><span data-stu-id="39d29-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="39d29-107">例子</span><span class="sxs-lookup"><span data-stu-id="39d29-107">EXAMPLES</span></span>

### <span data-ttu-id="39d29-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="39d29-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="39d29-109">從類型 "LocalUserNotAllowed" 建立新允許清單自訂通知 rull，狀態設為停用</span><span class="sxs-lookup"><span data-stu-id="39d29-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="39d29-110">參數</span><span class="sxs-lookup"><span data-stu-id="39d29-110">PARAMETERS</span></span>

### <span data-ttu-id="39d29-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="39d29-111">-AllowlistValue</span></span>
<span data-ttu-id="39d29-112">允許清單值。</span><span class="sxs-lookup"><span data-stu-id="39d29-112">Allow list values.</span></span>

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

### <span data-ttu-id="39d29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d29-113">-DefaultProfile</span></span>
<span data-ttu-id="39d29-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39d29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d29-115">-已啟用</span><span class="sxs-lookup"><span data-stu-id="39d29-115">-Enabled</span></span>
<span data-ttu-id="39d29-116">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="39d29-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="39d29-117">-類型</span><span class="sxs-lookup"><span data-stu-id="39d29-117">-Type</span></span>
<span data-ttu-id="39d29-118">規則類型。</span><span class="sxs-lookup"><span data-stu-id="39d29-118">Rule type.</span></span>

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

### <span data-ttu-id="39d29-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d29-119">CommonParameters</span></span>
<span data-ttu-id="39d29-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39d29-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d29-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39d29-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d29-122">輸入</span><span class="sxs-lookup"><span data-stu-id="39d29-122">INPUTS</span></span>

### <span data-ttu-id="39d29-123">沒有</span><span class="sxs-lookup"><span data-stu-id="39d29-123">None</span></span>

## <span data-ttu-id="39d29-124">輸出</span><span class="sxs-lookup"><span data-stu-id="39d29-124">OUTPUTS</span></span>

### <span data-ttu-id="39d29-125">Microsoft.Azure.Commands.security.models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="39d29-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="39d29-126">筆記</span><span class="sxs-lookup"><span data-stu-id="39d29-126">NOTES</span></span>

## <span data-ttu-id="39d29-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="39d29-127">RELATED LINKS</span></span>
