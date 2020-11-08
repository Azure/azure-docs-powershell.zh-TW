---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969076"
---
# <span data-ttu-id="069bb-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="069bb-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="069bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="069bb-102">SYNOPSIS</span></span>
<span data-ttu-id="069bb-103">為裝置安全性群組建立新的 [允許清單] 自訂警示規則 (IoT 安全性) </span><span class="sxs-lookup"><span data-stu-id="069bb-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="069bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="069bb-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="069bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="069bb-105">DESCRIPTION</span></span>
<span data-ttu-id="069bb-106">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject Cmdlet 會在 IoT security 方案中為 device security 群組建立一份新的允許自訂警報規則清單。</span><span class="sxs-lookup"><span data-stu-id="069bb-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="069bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="069bb-107">EXAMPLES</span></span>

### <span data-ttu-id="069bb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="069bb-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="069bb-109">從類型 "LocalUserNotAllowed" 建立新的 [允許清單] 自訂通知 rull，狀態設定為 [停用]</span><span class="sxs-lookup"><span data-stu-id="069bb-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="069bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="069bb-110">PARAMETERS</span></span>

### <span data-ttu-id="069bb-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="069bb-111">-AllowlistValue</span></span>
<span data-ttu-id="069bb-112">允許清單值。</span><span class="sxs-lookup"><span data-stu-id="069bb-112">Allow list values.</span></span>

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

### <span data-ttu-id="069bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="069bb-113">-DefaultProfile</span></span>
<span data-ttu-id="069bb-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="069bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="069bb-115">-啟用</span><span class="sxs-lookup"><span data-stu-id="069bb-115">-Enabled</span></span>
<span data-ttu-id="069bb-116">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="069bb-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="069bb-117">-類型</span><span class="sxs-lookup"><span data-stu-id="069bb-117">-Type</span></span>
<span data-ttu-id="069bb-118">規則類型。</span><span class="sxs-lookup"><span data-stu-id="069bb-118">Rule type.</span></span>

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

### <span data-ttu-id="069bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="069bb-119">CommonParameters</span></span>
<span data-ttu-id="069bb-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="069bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="069bb-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="069bb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="069bb-122">輸入</span><span class="sxs-lookup"><span data-stu-id="069bb-122">INPUTS</span></span>

### <span data-ttu-id="069bb-123">所有</span><span class="sxs-lookup"><span data-stu-id="069bb-123">None</span></span>

## <span data-ttu-id="069bb-124">輸出</span><span class="sxs-lookup"><span data-stu-id="069bb-124">OUTPUTS</span></span>

### <span data-ttu-id="069bb-125">PSAllowlistCustomAlertRule 中的 DeviceSecurityGroups （Security..。</span><span class="sxs-lookup"><span data-stu-id="069bb-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="069bb-126">筆記</span><span class="sxs-lookup"><span data-stu-id="069bb-126">NOTES</span></span>

## <span data-ttu-id="069bb-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="069bb-127">RELATED LINKS</span></span>