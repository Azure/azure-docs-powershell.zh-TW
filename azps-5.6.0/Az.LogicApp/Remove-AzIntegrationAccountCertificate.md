---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: f6e1d4d987ece31a91d119d1fe2ab781475fdc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904413"
---
# <span data-ttu-id="6ac89-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac89-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="6ac89-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ac89-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac89-103">從資源群組移除整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="6ac89-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="6ac89-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ac89-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ac89-105">描述</span><span class="sxs-lookup"><span data-stu-id="6ac89-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac89-106">**Remove-AzIficAccountCertificate** Cmdlet 會從資源群組移除整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="6ac89-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="6ac89-107">指定整合帳戶名稱、資源組名和憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac89-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="6ac89-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="6ac89-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6ac89-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="6ac89-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6ac89-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="6ac89-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6ac89-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="6ac89-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6ac89-112">例子</span><span class="sxs-lookup"><span data-stu-id="6ac89-112">EXAMPLES</span></span>

### <span data-ttu-id="6ac89-113">範例 1：移除整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="6ac89-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="6ac89-114">此命令會移除名為 IntegrationAccount31 的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="6ac89-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="6ac89-115">參數</span><span class="sxs-lookup"><span data-stu-id="6ac89-115">PARAMETERS</span></span>

### <span data-ttu-id="6ac89-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6ac89-116">-CertificateName</span></span>
<span data-ttu-id="6ac89-117">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac89-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="6ac89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac89-118">-DefaultProfile</span></span>
<span data-ttu-id="6ac89-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6ac89-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ac89-120">-強制</span><span class="sxs-lookup"><span data-stu-id="6ac89-120">-Force</span></span>
<span data-ttu-id="6ac89-121">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6ac89-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ac89-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ac89-122">-Name</span></span>
<span data-ttu-id="6ac89-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac89-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac89-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ac89-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac89-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac89-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6ac89-126">-Confirm</span></span>
<span data-ttu-id="6ac89-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6ac89-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac89-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac89-128">-WhatIf</span></span>
<span data-ttu-id="6ac89-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ac89-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ac89-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ac89-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac89-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac89-131">CommonParameters</span></span>
<span data-ttu-id="6ac89-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ac89-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac89-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6ac89-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac89-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6ac89-134">INPUTS</span></span>

### <span data-ttu-id="6ac89-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6ac89-135">System.String</span></span>

## <span data-ttu-id="6ac89-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6ac89-136">OUTPUTS</span></span>

### <span data-ttu-id="6ac89-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="6ac89-137">System.Void</span></span>

## <span data-ttu-id="6ac89-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6ac89-138">NOTES</span></span>

## <span data-ttu-id="6ac89-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ac89-139">RELATED LINKS</span></span>

[<span data-ttu-id="6ac89-140">Get-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac89-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="6ac89-141">New-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac89-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="6ac89-142">Set-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac89-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


