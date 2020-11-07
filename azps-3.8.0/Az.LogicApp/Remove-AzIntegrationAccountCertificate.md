---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966320"
---
# <span data-ttu-id="b4e39-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b4e39-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="b4e39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4e39-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e39-103">從資源群組中移除整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="b4e39-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="b4e39-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4e39-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e39-105">說明</span><span class="sxs-lookup"><span data-stu-id="b4e39-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e39-106">**AzIntegrationAccountCertificate** Cmdlet 會從資源群組中移除整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="b4e39-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="b4e39-107">指定整合帳戶名稱、資源群組名稱及憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e39-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="b4e39-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b4e39-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b4e39-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b4e39-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b4e39-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b4e39-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b4e39-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b4e39-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b4e39-112">示例</span><span class="sxs-lookup"><span data-stu-id="b4e39-112">EXAMPLES</span></span>

### <span data-ttu-id="b4e39-113">範例1：移除整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="b4e39-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="b4e39-114">這個命令會移除名為 IntegrationAccount31 的 integration 帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="b4e39-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="b4e39-115">參數</span><span class="sxs-lookup"><span data-stu-id="b4e39-115">PARAMETERS</span></span>

### <span data-ttu-id="b4e39-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b4e39-116">-CertificateName</span></span>
<span data-ttu-id="b4e39-117">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e39-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="b4e39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e39-118">-DefaultProfile</span></span>
<span data-ttu-id="b4e39-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b4e39-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4e39-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b4e39-120">-Force</span></span>
<span data-ttu-id="b4e39-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b4e39-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4e39-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4e39-122">-Name</span></span>
<span data-ttu-id="b4e39-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e39-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b4e39-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e39-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4e39-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4e39-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4e39-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b4e39-126">-Confirm</span></span>
<span data-ttu-id="b4e39-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b4e39-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e39-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e39-128">-WhatIf</span></span>
<span data-ttu-id="b4e39-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4e39-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4e39-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4e39-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e39-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e39-131">CommonParameters</span></span>
<span data-ttu-id="b4e39-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4e39-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e39-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4e39-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e39-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b4e39-134">INPUTS</span></span>

### <span data-ttu-id="b4e39-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b4e39-135">System.String</span></span>

## <span data-ttu-id="b4e39-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b4e39-136">OUTPUTS</span></span>

### <span data-ttu-id="b4e39-137">System.void</span><span class="sxs-lookup"><span data-stu-id="b4e39-137">System.Void</span></span>

## <span data-ttu-id="b4e39-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b4e39-138">NOTES</span></span>

## <span data-ttu-id="b4e39-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4e39-139">RELATED LINKS</span></span>

[<span data-ttu-id="b4e39-140">AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b4e39-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b4e39-141">新-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b4e39-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b4e39-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b4e39-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


