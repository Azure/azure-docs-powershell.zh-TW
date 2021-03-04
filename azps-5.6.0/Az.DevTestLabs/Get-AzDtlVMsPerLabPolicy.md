---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: fa19f45527302c858593d200fb2a6ed605d02321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907657"
---
# <span data-ttu-id="95133-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="95133-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="95133-102">簡介</span><span class="sxs-lookup"><span data-stu-id="95133-102">SYNOPSIS</span></span>
<span data-ttu-id="95133-103">在 DevTest 實驗室中，根據實驗室的實驗室策略，獲得虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95133-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="95133-104">語法</span><span class="sxs-lookup"><span data-stu-id="95133-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95133-105">描述</span><span class="sxs-lookup"><span data-stu-id="95133-105">DESCRIPTION</span></span>
<span data-ttu-id="95133-106">**Get-AzDtlVMsPerLabPolicy** Cmdlet 會根據實驗室的實驗室策略取得虛擬機器，這可讓您設定實驗室中允許的虛擬機器總數。</span><span class="sxs-lookup"><span data-stu-id="95133-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="95133-107">Cmdlet 會返回該策略的啟用或停用狀態，以及您于該政策中設定之實驗室所允許的虛擬機器總數。</span><span class="sxs-lookup"><span data-stu-id="95133-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="95133-108">例子</span><span class="sxs-lookup"><span data-stu-id="95133-108">EXAMPLES</span></span>

## <span data-ttu-id="95133-109">參數</span><span class="sxs-lookup"><span data-stu-id="95133-109">PARAMETERS</span></span>

### <span data-ttu-id="95133-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95133-110">-DefaultProfile</span></span>
<span data-ttu-id="95133-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="95133-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95133-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="95133-112">-LabName</span></span>
<span data-ttu-id="95133-113">指定此 Cmdlet 可獲取虛擬機器的實驗室名稱。</span><span class="sxs-lookup"><span data-stu-id="95133-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="95133-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95133-114">-ResourceGroupName</span></span>
<span data-ttu-id="95133-115">指定實驗室所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="95133-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="95133-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95133-116">CommonParameters</span></span>
<span data-ttu-id="95133-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="95133-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95133-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="95133-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95133-119">輸入</span><span class="sxs-lookup"><span data-stu-id="95133-119">INPUTS</span></span>

### <span data-ttu-id="95133-120">System.String</span><span class="sxs-lookup"><span data-stu-id="95133-120">System.String</span></span>

## <span data-ttu-id="95133-121">輸出</span><span class="sxs-lookup"><span data-stu-id="95133-121">OUTPUTS</span></span>

### <span data-ttu-id="95133-122">Microsoft.Azure.Commands.DevTestLabs.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="95133-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="95133-123">筆記</span><span class="sxs-lookup"><span data-stu-id="95133-123">NOTES</span></span>

## <span data-ttu-id="95133-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="95133-124">RELATED LINKS</span></span>

[<span data-ttu-id="95133-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="95133-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


