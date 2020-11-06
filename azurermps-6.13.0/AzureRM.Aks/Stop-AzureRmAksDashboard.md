---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 719ef5fd3676fdc5d5b6b8460bcb3edafabb83f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448509"
---
# <span data-ttu-id="bf0cc-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="bf0cc-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="bf0cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0cc-103">停止在 Start-AzureRmKubernetesDashboard 中建立的 Kubectl SSH 隧道。</span><span class="sxs-lookup"><span data-stu-id="bf0cc-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf0cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf0cc-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf0cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="bf0cc-106">停止在 Start-AzureRmKubernetesDashboard 中建立的 Kubectl SSH 隧道。</span><span class="sxs-lookup"><span data-stu-id="bf0cc-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="bf0cc-107">示例</span><span class="sxs-lookup"><span data-stu-id="bf0cc-107">EXAMPLES</span></span>

### <span data-ttu-id="bf0cc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bf0cc-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="bf0cc-109">執行 Start-AzureRmKubernetesDashboard，以停止現有的 SSH 隧道設定。</span><span class="sxs-lookup"><span data-stu-id="bf0cc-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="bf0cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf0cc-110">PARAMETERS</span></span>

### <span data-ttu-id="bf0cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0cc-111">-DefaultProfile</span></span>
<span data-ttu-id="bf0cc-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf0cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0cc-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf0cc-113">-PassThru</span></span>
<span data-ttu-id="bf0cc-114">如果 SSH 隧道已關閉，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="bf0cc-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="bf0cc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0cc-115">CommonParameters</span></span>
<span data-ttu-id="bf0cc-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf0cc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0cc-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf0cc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0cc-118">輸入</span><span class="sxs-lookup"><span data-stu-id="bf0cc-118">INPUTS</span></span>

### <span data-ttu-id="bf0cc-119">所有</span><span class="sxs-lookup"><span data-stu-id="bf0cc-119">None</span></span>

## <span data-ttu-id="bf0cc-120">輸出</span><span class="sxs-lookup"><span data-stu-id="bf0cc-120">OUTPUTS</span></span>

### <span data-ttu-id="bf0cc-121">System.object</span><span class="sxs-lookup"><span data-stu-id="bf0cc-121">System.Boolean</span></span>

## <span data-ttu-id="bf0cc-122">筆記</span><span class="sxs-lookup"><span data-stu-id="bf0cc-122">NOTES</span></span>

## <span data-ttu-id="bf0cc-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf0cc-123">RELATED LINKS</span></span>
