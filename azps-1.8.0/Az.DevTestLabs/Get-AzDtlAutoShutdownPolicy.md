---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622398"
---
# <span data-ttu-id="17fef-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="17fef-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="17fef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17fef-102">SYNOPSIS</span></span>
<span data-ttu-id="17fef-103">在 DevTest 實驗中取得實驗室的自動關閉原則。</span><span class="sxs-lookup"><span data-stu-id="17fef-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="17fef-104">句法</span><span class="sxs-lookup"><span data-stu-id="17fef-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17fef-105">說明</span><span class="sxs-lookup"><span data-stu-id="17fef-105">DESCRIPTION</span></span>
<span data-ttu-id="17fef-106">**AzDtlAutoShutdownPolicy** Cmdlet 會取得 lab 的自動關閉原則，這可讓您在一天中的指定時間自動關閉實驗室中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="17fef-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="17fef-107">此 Cmdlet 會傳回是否已啟用原則的狀態，以及您設定為自動關閉實驗室虛擬機器的時間。</span><span class="sxs-lookup"><span data-stu-id="17fef-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="17fef-108">示例</span><span class="sxs-lookup"><span data-stu-id="17fef-108">EXAMPLES</span></span>

## <span data-ttu-id="17fef-109">參數</span><span class="sxs-lookup"><span data-stu-id="17fef-109">PARAMETERS</span></span>

### <span data-ttu-id="17fef-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fef-110">-DefaultProfile</span></span>
<span data-ttu-id="17fef-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="17fef-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17fef-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="17fef-112">-LabName</span></span>
<span data-ttu-id="17fef-113">指定此 Cmdlet 取得自動關閉原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="17fef-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="17fef-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fef-114">-ResourceGroupName</span></span>
<span data-ttu-id="17fef-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17fef-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="17fef-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fef-116">CommonParameters</span></span>
<span data-ttu-id="17fef-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17fef-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fef-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17fef-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fef-119">輸入</span><span class="sxs-lookup"><span data-stu-id="17fef-119">INPUTS</span></span>

### <span data-ttu-id="17fef-120">System.object</span><span class="sxs-lookup"><span data-stu-id="17fef-120">System.String</span></span>

## <span data-ttu-id="17fef-121">輸出</span><span class="sxs-lookup"><span data-stu-id="17fef-121">OUTPUTS</span></span>

### <span data-ttu-id="17fef-122">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="17fef-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="17fef-123">筆記</span><span class="sxs-lookup"><span data-stu-id="17fef-123">NOTES</span></span>

## <span data-ttu-id="17fef-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="17fef-124">RELATED LINKS</span></span>

[<span data-ttu-id="17fef-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="17fef-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


