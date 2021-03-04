---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 7c2a7ef4c134d811d8c30266305f25d3d53b1289
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915505"
---
# <span data-ttu-id="829ac-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="829ac-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="829ac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="829ac-102">SYNOPSIS</span></span>
<span data-ttu-id="829ac-103">在 DevTest 實驗室中，根據實驗室的使用者策略，獲得虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="829ac-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="829ac-104">語法</span><span class="sxs-lookup"><span data-stu-id="829ac-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="829ac-105">描述</span><span class="sxs-lookup"><span data-stu-id="829ac-105">DESCRIPTION</span></span>
<span data-ttu-id="829ac-106">**Get-AzDtlVMsPerUserPolicy** Cmdlet 會取得實驗室每個使用者策略的虛擬機器，這可讓您設定每個使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="829ac-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="829ac-107">Cmdlet 會返回該策略的啟用或停用狀態，以及您于該政策中設定之每個使用者允許的虛擬機器數目上限。</span><span class="sxs-lookup"><span data-stu-id="829ac-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="829ac-108">例子</span><span class="sxs-lookup"><span data-stu-id="829ac-108">EXAMPLES</span></span>

## <span data-ttu-id="829ac-109">參數</span><span class="sxs-lookup"><span data-stu-id="829ac-109">PARAMETERS</span></span>

### <span data-ttu-id="829ac-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829ac-110">-DefaultProfile</span></span>
<span data-ttu-id="829ac-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="829ac-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="829ac-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="829ac-112">-LabName</span></span>
<span data-ttu-id="829ac-113">指定此 Cmdlet 會針對每個使用者策略獲得虛擬機器的實驗室名稱。</span><span class="sxs-lookup"><span data-stu-id="829ac-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="829ac-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="829ac-114">-ResourceGroupName</span></span>
<span data-ttu-id="829ac-115">指定實驗室所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="829ac-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="829ac-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829ac-116">CommonParameters</span></span>
<span data-ttu-id="829ac-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="829ac-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829ac-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="829ac-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829ac-119">輸入</span><span class="sxs-lookup"><span data-stu-id="829ac-119">INPUTS</span></span>

### <span data-ttu-id="829ac-120">System.String</span><span class="sxs-lookup"><span data-stu-id="829ac-120">System.String</span></span>

## <span data-ttu-id="829ac-121">輸出</span><span class="sxs-lookup"><span data-stu-id="829ac-121">OUTPUTS</span></span>

### <span data-ttu-id="829ac-122">Microsoft.Azure.Commands.DevTestLabs.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="829ac-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="829ac-123">筆記</span><span class="sxs-lookup"><span data-stu-id="829ac-123">NOTES</span></span>

## <span data-ttu-id="829ac-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="829ac-124">RELATED LINKS</span></span>

[<span data-ttu-id="829ac-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="829ac-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


