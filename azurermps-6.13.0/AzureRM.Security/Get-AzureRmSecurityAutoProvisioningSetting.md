---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625250"
---
# <span data-ttu-id="b44ed-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b44ed-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b44ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b44ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b44ed-103">取得安全性自動提供設定</span><span class="sxs-lookup"><span data-stu-id="b44ed-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b44ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="b44ed-104">SYNTAX</span></span>

### <span data-ttu-id="b44ed-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="b44ed-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b44ed-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b44ed-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b44ed-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b44ed-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b44ed-108">說明</span><span class="sxs-lookup"><span data-stu-id="b44ed-108">DESCRIPTION</span></span>
<span data-ttu-id="b44ed-109">自動提供設定可讓您決定是否要讓 Azure Security Cetner 自動 proviosion 將在 Vm 上安裝的安全代理程式。</span><span class="sxs-lookup"><span data-stu-id="b44ed-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="b44ed-110">安全性代理程式會監視您的 VM，以建立安全警示，並監視 VM 的安全性合規性。</span><span class="sxs-lookup"><span data-stu-id="b44ed-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="b44ed-111">示例</span><span class="sxs-lookup"><span data-stu-id="b44ed-111">EXAMPLES</span></span>

### <span data-ttu-id="b44ed-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b44ed-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="b44ed-113">取得訂閱的自動預配設定</span><span class="sxs-lookup"><span data-stu-id="b44ed-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="b44ed-114">參數</span><span class="sxs-lookup"><span data-stu-id="b44ed-114">PARAMETERS</span></span>

### <span data-ttu-id="b44ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44ed-115">-DefaultProfile</span></span>
<span data-ttu-id="b44ed-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b44ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44ed-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b44ed-117">-Name</span></span>
<span data-ttu-id="b44ed-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b44ed-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44ed-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b44ed-119">-ResourceId</span></span>
<span data-ttu-id="b44ed-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b44ed-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b44ed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44ed-121">CommonParameters</span></span>
<span data-ttu-id="b44ed-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b44ed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44ed-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b44ed-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44ed-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b44ed-124">INPUTS</span></span>

### <span data-ttu-id="b44ed-125">System.object</span><span class="sxs-lookup"><span data-stu-id="b44ed-125">System.String</span></span>

## <span data-ttu-id="b44ed-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b44ed-126">OUTPUTS</span></span>

### <span data-ttu-id="b44ed-127">PSSecurityAutoProvisioningSetting 中的 AutoProvisioningSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="b44ed-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b44ed-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b44ed-128">NOTES</span></span>

## <span data-ttu-id="b44ed-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b44ed-129">RELATED LINKS</span></span>
