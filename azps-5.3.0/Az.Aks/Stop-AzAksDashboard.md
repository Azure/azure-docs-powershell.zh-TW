---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437740"
---
# <span data-ttu-id="9c288-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="9c288-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="9c288-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c288-102">SYNOPSIS</span></span>
<span data-ttu-id="9c288-103">停止在 Start-AzKubernetesDashboard 中建立的 Kubectl SSH 隧道。</span><span class="sxs-lookup"><span data-stu-id="9c288-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="9c288-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c288-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c288-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c288-105">DESCRIPTION</span></span>
<span data-ttu-id="9c288-106">停止在 Start-AzKubernetesDashboard 中建立的 Kubectl SSH 隧道。</span><span class="sxs-lookup"><span data-stu-id="9c288-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="9c288-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c288-107">EXAMPLES</span></span>

### <span data-ttu-id="9c288-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9c288-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="9c288-109">執行 Start-AzKubernetesDashboard，以停止現有的 SSH 隧道設定。</span><span class="sxs-lookup"><span data-stu-id="9c288-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="9c288-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c288-110">PARAMETERS</span></span>

### <span data-ttu-id="9c288-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c288-111">-DefaultProfile</span></span>
<span data-ttu-id="9c288-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c288-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c288-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c288-113">-PassThru</span></span>
<span data-ttu-id="9c288-114">如果 SSH 隧道已關閉，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="9c288-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="9c288-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c288-115">CommonParameters</span></span>
<span data-ttu-id="9c288-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c288-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c288-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9c288-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c288-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9c288-118">INPUTS</span></span>

### <span data-ttu-id="9c288-119">所有</span><span class="sxs-lookup"><span data-stu-id="9c288-119">None</span></span>

## <span data-ttu-id="9c288-120">輸出</span><span class="sxs-lookup"><span data-stu-id="9c288-120">OUTPUTS</span></span>

### <span data-ttu-id="9c288-121">System.object</span><span class="sxs-lookup"><span data-stu-id="9c288-121">System.Boolean</span></span>

## <span data-ttu-id="9c288-122">筆記</span><span class="sxs-lookup"><span data-stu-id="9c288-122">NOTES</span></span>

## <span data-ttu-id="9c288-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c288-123">RELATED LINKS</span></span>
